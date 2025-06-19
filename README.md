# SlydenartsB
Slydenarts jarvis
<xml xmlns="http://www.w3.org/1999/xhtml" is_dbot="true" collection="false">

  <variables>

    <variable type="" id="VLBj7P@:FqNy~,R[c9Hp">Prediction</variable>

    <variable type="" id="}4sS3G-ig-*lgLxN.HK~">Entry Point</variable>

    <variable type="" id="r3#,*L{|k_*_oikco?~E">Stake</variable>

    <variable type="" id="Qq28jzu{61V^?3_DKY1z">text</variable>

    <variable type="" id="!(67Y!ov*~[U/$pjZ,0.">Stake win</variable>

    <variable type="" id="x4khAyN_n|huu=qVhBFG">item</variable>

    <variable type="" id="Z@.ow_sBjxwtbL$F52.u">Martingale</variable>

    <variable type="" id="_$b#PTe$SH2iW}Unna2W">Use Martingale</variable>

    <variable type="" id="iexW!(p-QSL[kDvWK`o-">Take Profit</variable>

    <variable type="" id="AwGIX3K`=6@AOl/-`G)O">Stop Loss</variable>

    <variable type="" id="tpKgmnH0mz*.t/T=*i|V">Maximum Runs</variable>

    <variable type="" id="XfX?ed24Y,S7*f=/-sQ9">Use Compounding Stake</variable>

    <variable type="" id="@VN/)JBDaz5d-aHKEiy:">Switch Markets</variable>

    <variable type="" id="Vd)a}rnFL$Mr`V[FG0ZX">Count</variable>

    <variable type="" id=":,%~KY@s+t4t[x%D|Rs`">Set Maximum Runs</variable>

    <variable type="" id="nL}rZqx,y/BJNYaP$b:T">Next trade</variable>

    <variable type="" id="kv1LrCbomC4@7:M/d%?0">Use Contract Type Switcher</variable>

    <variable type="" id="EyYZFSoOM?_MS_~x:Z^(">Stop Trading on loss</variable>

    <variable type="" id="S58/v7q-;.szsCzu^Vvo">Total Lost</variable>

    <variable type="" id="ITcU7:kSbe)cNBWn8K#R">Count Loss</variable>

    <variable type="" id="new_digit_freq">Digit Frequency</variable>

    <variable type="" id="new_market_winrate">Market Winrate</variable>

  </variables>

  <block type="trade_definition" id="Dn+|l@F{1c%e:[S_b*y+" deletable="false" x="0" y="60">

    <statement name="TRADE_OPTIONS">

      <block type="trade_definition_market" id="?%-k%1.^XwP?^NTZ,Yt%">

        <field name="MARKET_LIST">synthetic_index</field>

        <field name="SUBMARKET_LIST">random_index</field>

        <field name="SYMBOL_LIST">1HZ10V</field>

        <next>

          <block type="trade_definition_tradetype" id="Ny,T+]j~q=euwb2^Hkrt">

            <field name="TRADETYPECAT_LIST">digits</field>

            <field name="TRADETYPE_LIST">overunder</field>

            <next>

              <block type="trade_definition_contracttype" id="9KwoosLzczeC~F:5~JTl">

                <field name="TYPE_LIST">both</field>

                <next>

                  <block type="trade_definition_candleinterval" id="YCRtYsVDuvI2m(|Sn=oN">

                    <field name="CANDLEINTERVAL_LIST">60</field>

                    <next>

                      <block type="trade_definition_restartbuysell" id="5Nn9BCfR{SxZMWof=~U6">

                        <field name="TIME_MACHINE_ENABLED">FALSE</field>

                        <next>

                          <block type="trade_definition_restartonerror" id="$w}(v#RJo+GTV~6N#rJ(">

                            <field name="RESTARTONERROR">TRUE</field>

                          </block>

                        </next>

                      </block>

                    </next>

                  </block>

                </next>

              </block>

            </next>

          </block>

        </next>

      </block>

    </statement>

    <statement name="INITIALIZATION">

      <block type="variables_set" id="VtinTUlRho|l^-0R$7%A">

        <field name="VAR" id="r3#,*L{|k_*_oikco?~E">Stake</field>

        <value name="VALUE">

          <block type="math_number" id="eE1:{)l/a]lYGgEq(xNf">

            <field name="NUM">0.5</field>

          </block>

        </value>

        <next>

          <block type="variables_set" id="yuTs63H@^mt2$7WA8MM#">

            <field name="VAR" id="iexW!(p-QSL[kDvWK`o-">Take Profit</field>

            <value name="VALUE">

              <block type="math_number" id="Ze7;s[0;Nz2%O4S_83gA">

                <field name="NUM">5</field>

              </block>

            </value>

            <next>

              <block type="variables_set" id="nGr}CP0n6hP98*@D%p1~">

                <field name="VAR" id="AwGIX3K`=6@AOl/-`G)O">Stop Loss</field>

                <value name="VALUE">

                  <block type="math_number" id="CNwP055C@dZ]pl;V~^@e">

                    <field name="NUM">30</field>

                  </block>

                </value>

                <next>

                  <block type="variables_set" id="OsGf7Gg0%Bcr(O%2{xCZ">

                    <field name="VAR" id="Z@.ow_sBjxwtbL$F52.u">Martingale</field>

                    <value name="VALUE">

                      <block type="math_number" id="A:w{a,.n|YO,bwZCpH[w">

                        <field name="NUM">2</field>

                      </block>

                    </value>

                    <next>

                      <block type="variables_set" id="l!28PD.;#a94j}-Zny(w">

                        <field name="VAR" id="_$b#PTe$SH2iW}Unna2W">Use Martingale</field>

                        <value name="VALUE">

                          <block type="logic_boolean" id="yGRw;hhT=8$k[bq6[a5v">

                            <field name="BOOL">TRUE</field>

                          </block>

                        </value>

                        <next>

                          <block type="variables_set" id="if+z)P.pg^EiMjJbZURL">

                            <field name="VAR" id="XfX?ed24Y,S7*f=/-sQ9">Use Compounding Stake</field>

                            <value name="VALUE">

                              <block type="logic_boolean" id="#q7dU*x-S3?p7GPK0lX)">

                                <field name="BOOL">FALSE</field>

                              </block>

                            </value>

                            <next>

                              <block type="variables_set" id="I-tw}E3wa6t2?-7un5%W">

                                <field name="VAR" id="@VN/)JBDaz5d-aHKEiy:">Switch Markets</field>

                                <value name="VALUE">

                                  <block type="logic_boolean" id="nEAPjl%ws7=.-TTk$d5j">

                                    <field name="BOOL">TRUE</field>

                                  </block>

                                </value>

                                <next>

                                  <block type="variables_set" id="Eu_!a.GW35dfWcQJT{Vo">

                                    <field name="VAR" id=":,%~KY@s+t4t[x%D|Rs`">Set Maximum Runs</field>

                                    <value name="VALUE">

                                      <block type="logic_boolean" id="/bG]-A`uutQSD($fK!W*">

                                        <field name="BOOL">TRUE</field>

                                      </block>

                                    </value>

                                    <next>

                                      <block type="variables_set" id="3ry|G9dufBVWni)wW5~^">

                                        <field name="VAR" id="kv1LrCbomC4@7:M/d%?0">Use Contract Type Switcher</field>

                                        <value name="VALUE">

                                          <block type="logic_boolean" id="S]DG$Gq*/`RUC]^?l6W1">

                                            <field name="BOOL">TRUE</field>

                                          </block>

                                        </value>

                                        <next>

                                          <block type="variables_set" id="+|3)-`f/qVr`m0B0;z(d">

                                            <field name="VAR" id="EyYZFSoOM?_MS_~x:Z^(">Stop Trading on loss</field>

                                            <value name="VALUE">

                                              <block type="logic_boolean" id="HL_;+VpMGGdymGC[NN%7">

                                                <field name="BOOL">TRUE</field>

                                              </block>

                                            </value>

                                            <next>

                                              <block type="variables_set" id="cDt^{%2b6}0F^KwAWoZ|">

                                                <field name="VAR" id="nL}rZqx,y/BJNYaP$b:T">Next trade</field>

                                                <value name="VALUE">

                                                  <block type="text" id="7-dU{:DF[`~${DPrwRqd">

                                                    <field name="TEXT">Under</field>

                                                  </block>

                                                </value>

                                                <next>

                                                  <block type="variables_set" id="04?NsjPy@EcVaNBFvS~q">

                                                    <field name="VAR" id="!(67Y!ov*~[U/$pjZ,0.">Stake win</field>

                                                    <value name="VALUE">

                                                      <block type="variables_get" id="x|YP+!A%~5?j+94P(AuL">

                                                        <field name="VAR" id="r3#,*L{|k_*_oikco?~E">Stake</field>

                                                      </block>

                                                    </value>

                                                    <next>

                                                      <block type="variables_set" id=",N%:N5HXk:D9]dYCQJ-N">

                                                        <field name="VAR" id="Vd)a}rnFL$Mr`V[FG0ZX">Count</field>

                                                        <value name="VALUE">

                                                          <block type="math_number" id="%dG/.3}`9pxjxDYvt3t$">

                                                            <field name="NUM">0</field>

                                                          </block>

                                                        </value>

                                                        <next>

                                                          <block type="variables_set" id="init_max_runs">

                                                            <field name="VAR" id="tpKgmnH0mz*.t/T=*i|V">Maximum Runs</field>

                                                            <value name="VALUE">

                                                              <block type="math_number" id="max_runs_value">

                                                                <field name="NUM">5</field>

                                                              </block>

                                                            </value>

                                                            <next>

                                                              <block type="variables_set" id="init_entry_point">

                                                                <field name="VAR" id="}4sS3G-ig-*lgLxN.HK~">Entry Point</field>

                                                                <value name="VALUE">

                                                                  <block type="math_number" id="entry_point_value">

                                                                    <field name="NUM">0</field>

                                                                  </block>

                                                                </value>

                                                                <next>

                                                                  <block type="variables_set" id="init_digit_freq">

                                                                    <field name="VAR" id="new_digit_freq">Digit Frequency</field>

                                                                    <value name="VALUE">

                                                                      <block type="lists_create_with" id="digit_freq_list">

                                                                        <mutation items="10"></mutation>

                                                                        <value name="ADD0">

                                                                          <block type="math_number" id="freq_0"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD1">

                                                                          <block type="math_number" id="freq_1"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD2">

                                                                          <block type="math_number" id="freq_2"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD3">

                                                                          <block type="math_number" id="freq_3"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD4">

                                                                          <block type="math_number" id="freq_4"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD5">

                                                                          <block type="math_number" id="freq_5"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD6">

                                                                          <block type="math_number" id="freq_6"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD7">

                                                                          <block type="math_number" id="freq_7"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD8">

                                                                          <block type="math_number" id="freq_8"><field name="NUM">0</field></block>

                                                                        </value>

                                                                        <value name="ADD9">

                                                                          <block type="math_number" id="freq_9"><field name="NUM">0</field></block>

                                                                        </value>

                                                                      </block>

                                                                    </value>

                                                                    <next>

                                                                      <block type="variables_set" id="init_market_winrate">

                                                                        <field name="VAR" id="new_market_winrate">Market Winrate</field>

                                                                        <value name="VALUE">

                                                                          <block type="lists_create_with" id="market_winrate_list">

                                                                            <mutation items="10"></mutation>

                                                                            <value name="ADD0">

                                                                              <block type="math_number" id="winrate_1hz10v"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD1">

                                                                              <block type="math_number" id="winrate_r10"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD2">

                                                                              <block type="math_number" id="winrate_1hz25v"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD3">

                                                                              <block type="math_number" id="winrate_r25"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD4">

                                                                              <block type="math_number" id="winrate_1hz50v"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD5">

                                                                              <block type="math_number" id="winrate_r50"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD6">

                                                                              <block type="math_number" id="winrate_1hz75v"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD7">

                                                                              <block type="math_number" id="winrate_r75"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD8">

                                                                              <block type="math_number" id="winrate_1hz100v"><field name="NUM">0</field></block>

                                                                            </value>

                                                                            <value name="ADD9">

                                                                              <block type="math_number" id="winrate_r100"><field name="NUM">0</field></block>

                                                                            </value>

                                                                          </block>

                                                                        </value>

                                                                        <next>

                                                                          <block type="procedures_callnoreturn" id="n5,AF[HWnBb[AxF:2sMU">

                                                                            <mutation name="Prevent Over Trading"></mutation>

                                                                            <data>:Tq]VUlM=BJk#=;.3aYU</data>

                                                                          </block>

                                                                        </next>

                                                                      </block>

                                                                    </next>

                                                                  </block>

                                                                </next>

                                                              </block>

                                                            </next>

                                                          </block>

                                                        </next>

                                                      </block>

                                                    </next>

                                                  </block>

                                                </next>

                                              </block>

                                            </next>

                                          </block>

                                        </next>

                                      </block>

                                    </next>

                                  </block>

                                </next>

                              </block>

                            </next>

                          </block>

                        </next>

                      </block>

                    </next>

                  </block>

                </next>

              </block>

            </next>

          </block>

        </next>

      </block>

    </statement>

    <statement name="SUBMARKET">

      <block type="controls_if" id="anmDpxw5Adhq9v~h]Awq">

        <mutation else="1"></mutation>

        <value name="IF0">

          <block type="logic_compare" id="b8o))xezc!K1;?$UIb2$">

            <field name="OP">EQ</field>

            <value name="A">

              <block type="variables_get" id="Ij=X5uP[Ioqg61An4!x*">

                <field name="VAR" id="kv1LrCbomC4@7:M/d%?0">Use Contract Type Switcher</field>

              </block>

            </value>

            <value name="B">

              <block type="logic_boolean" id="`@^14BdMpg~Q?vvHO^,v">

                <field name="BOOL">TRUE</field>

              </block>

            </value>

          </block>

        </value>

        <statement name="DO0">

          <block type="controls_if" id="4yuK|P)X[jgCh+,5iS,#">

            <mutation else="1"></mutation>

            <value name="IF0">

              <block type="logic_compare" id="jj7?J?-_ya[J9E,+#%Cc">

                <field name="OP">EQ</field>

                <value name="A">

                  <block type="variables_get" id="KzAX8!g|YUmkj_wV3w0o">

                    <field name="VAR" id="nL}rZqx,y/BJNYaP$b:T">Next trade</field>

                  </block>

                </value>

                <value name="B">

                  <block type="text" id="[y5t1B%WCT58;li9$q)|">

                    <field name="TEXT">Under</field>

                  </block>

                </value>

              </block>

            </value>

            <statement name="DO0">

              <block type="trade_definition_tradeoptions" id="WeNX1fen.XO?FdRLm_m^">

                <mutation has_first_barrier="false" has_second_barrier="false" has_prediction="true"></mutation>

                <field name="DURATIONTYPE_LIST">t</field>

                <value name="DURATION">

                  <block type="math_number_positive" id="},}3yJ69-J-gHxwa*8N:">

                    <field name="NUM">1</field>

                  </block>

                </value>

                <value name="AMOUNT">

                  <block type="variables_get" id="#=u;*~XqDVf(6j+LY9ZD">

                    <field name="VAR" id="r3#,*L{|k_*_oikco?~E">Stake</field>

                  </block>

                </value>

                <value name="PREDICTION">

                  <block type="variables_get" id="predict_digit_under">

                    <field name="VAR" id="VLBj7P@:FqNy~,R[c9Hp">Prediction</field>

                  </block>

                </value>

              </block>

            </statement>

            <statement name="ELSE">

              <block type="trade_definition_tradeoptions" id=")2;2*D/$2pgX[q!*kxgp">

                <mutation has_first_barrier="false" has_second_barrier="false" has_prediction="true"></mutation>

                <field name="DURATIONTYPE_LIST">t</field>

                <value name="DURATION">

                  <block type="math_number_positive" id=":D]*%PuYHSi,!G?lp.GK">

                    <field name="NUM">1</field>

                  </block>

                </value>

                <value name="AMOUNT">

                  <block type="variables_get" id="yps9ix^qx%0T]|pcs668">

                    <field name="VAR" id="r3#,*L{|k_*_oikco?~E">Stake</field>

                  </block>

                </value>

                <value name="PREDICTION">

                  <block type="variables_get" id="predict_digit_over">

                    <field name="VAR" id="VLBj7P@:FqNy~,R[c9Hp">Prediction</field>

                  </block>

                </value>

              </block>

            </statement>

          </block>

        </statement>

        <statement name="ELSE">

          <block type="trade_definition_tradeoptions" id="@e5eu8)vsyZoeZ9bq:l2">

            <mutation has_first_barrier="false" has_second_barrier="false" has_prediction="true"></mutation>

            <field name="DURATIONTYPE_LIST">t</field>

            <value name="DURATION">

              <block type="math_number_positive" id="[-?H:mw.%kyE)RM_35B`">

                <field name="NUM">1</field>

              </block>

            </value>

            <value name="AMOUNT">

              <block type="variables_get" id="U6xds)Q]hxNbdDih)t-:">

                <field name="VAR" id="r3#,*L{|k_*_oikco?~E">Stake</field>

              </block>

            </value>

            <value name="PREDICTION">

              <block type="variables_get" id="predict_digit_default">

                <field name="VAR" id="VLBj7P@:FqNy~,R[c9Hp">Prediction</field>

              </block>

            </value>

          </block>

        </statement>

      </block>

    </statement>

  </block>

  <block type="before_purchase" id="V/jf;#b@;*@3ATM]D)=;" deletable="false" x="0" y="1716">

    <statement name="BEFOREPURCHASE_STACK">

      <block type="variables_set" id="reset_digit_freq">

        <field name="VAR" id="new_digit_freq">Digit Frequency</field>

        <value name="VALUE">

          <block type="lists_create_with" id="reset_freq_list">

            <mutation items="10"></mutation>

            <value name
