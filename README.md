- 👋 Hi, I’m @Shoun22
<xml xmlns="http://www.w3.org/1999/xhtml" collection="false">
  <variables>
    <variable type="" id="3C@HUF)?z(zn8g3GPaNd">TARGET PROFIT</variable>
    <variable type="" id="/|o~W%gQIAM#UHZO!zA*">STAKE_MODAL</variable>
    <variable type="" id="nfN(I4pYa%!hdG-=ekrk">Initial Stake</variable>
    <variable type="" id="~12olgeNy)D^x^u7$b{o">PREDIKSI</variable>
    <variable type="" id="+e9-IVuJ/mv#4%/,MX2r">STOP_LOSS</variable>
    <variable type="" id="WB^wGp{On}ZKq/4LK4Ca">MARTI</variable>
  </variables>
  <block type="trade" id="xgH69|xFn9=70w.*3Vo@" x="0" y="0">
    <field name="MARKET_LIST">synthetic_index</field>
    <field name="SUBMARKET_LIST">random_index</field>
    <field name="SYMBOL_LIST">R_10</field>
    <field name="TRADETYPECAT_LIST">digits</field>
    <field name="TRADETYPE_LIST">overunder</field>
    <field name="TYPE_LIST">DIGITOVER</field>
    <field name="CANDLEINTERVAL_LIST">60</field>
    <field name="TIME_MACHINE_ENABLED">FALSE</field>
    <field name="RESTARTONERROR">TRUE</field>
    <statement name="INITIALIZATION">
      <block type="variables_set" id="Xi/7unh.Wda86Y+ho3di">
        <field name="VAR" id="3C@HUF)?z(zn8g3GPaNd" variabletype="">TARGET PROFIT</field>
        <value name="VALUE">
          <block type="math_number" id="6[{b4,~Ah7?6uSJYqr4@">
            <field name="NUM">5</field>
          </block>
        </value>
        <next>
          <block type="variables_set" id="c-||aYScR/g!vo~{/X[e">
            <field name="VAR" id="/|o~W%gQIAM#UHZO!zA*" variabletype="">STAKE_MODAL</field>
            <value name="VALUE">
              <block type="math_number" id="g~[uqoN*x_reSg69qAb(">
                <field name="NUM">0.5</field>
              </block>
            </value>
            <next>
              <block type="variables_set" id="tSdo88{{x|bkDDqQ5[PB">
                <field name="VAR" id="+e9-IVuJ/mv#4%/,MX2r" variabletype="">STOP_LOSS</field>
                <value name="VALUE">
                  <block type="math_number" id="aQF}bz#EW1!ExO/XqCjP">
                    <field name="NUM">50</field>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="Au[U|iv$}Dv%Oao?|=T?">
                    <field name="VAR" id="WB^wGp{On}ZKq/4LK4Ca" variabletype="">MARTI</field>
                    <value name="VALUE">
                      <block type="math_number" id="o5g6@SNiXs|W~D`t9~dm">
                        <field name="NUM">1.5</field>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id="e1s%c0-U@@6w%FE6ER#w">
                        <field name="VAR" id="~12olgeNy)D^x^u7$b{o" variabletype="">PREDIKSI</field>
                        <value name="VALUE">
                          <block type="math_number" id="I]astph|SH-$GT,j|bqc">
                            <field name="NUM">3</field>
                          </block>
                        </value>
                        <next>
                          <block type="variables_set" id="XkO1?ufjD(|LFlLW(E[)" collapsed="true">
                            <field name="VAR" id="nfN(I4pYa%!hdG-=ekrk" variabletype="">Initial Stake</field>
                            <value name="VALUE">
                              <block type="variables_get" id="=5^x@X=lSNbjZLM{ieBe">
                                <field name="VAR" id="/|o~W%gQIAM#UHZO!zA*" variabletype="">STAKE_MODAL</field>
                              </block>
                            </value>
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
      <block type="tradeOptions" id="zB3=PkD2eZ%X%(f9v-*E">
        <field name="DURATIONTYPE_LIST">t</field>
        <field name="CURRENCY_LIST">USD</field>
        <field name="BARRIEROFFSETTYPE_LIST">+</field>
        <field name="SECONDBARRIEROFFSETTYPE_LIST">-</field>
        <value name="DURATION">
          <shadow type="math_number" id="5V-_Pm5hl%K|AyV01I2o">
            <field name="NUM">2</field>
          </shadow>
        </value>
        <value name="AMOUNT">
          <shadow type="math_number" id="$E8jCr1ln#4ykRe?A.-{">
            <field name="NUM">1</field>
          </shadow>
          <block type="variables_get" id="W3)vI$+sC,kZbk1U[IRb">
            <field name="VAR" id="nfN(I4pYa%!hdG-=ekrk" variabletype="">Initial Stake</field>
          </block>
        </value>
        <value name="PREDICTION">
          <shadow type="math_number" id="/^!rgI/6k_8lZnmSf41M">
            <field name="NUM">0</field>
          </shadow>
          <block type="variables_get" id="NsP7qJW_9ZB8Q#kXII|8">
            <field name="VAR" id="~12olgeNy)D^x^u7$b{o" variabletype="">PREDIKSI</field>
          </block>
        </value>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="i-CIx.(Onm4?ihxzA}Y]" x="0" y="609">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="controls_if" id="Es!hhZ{Ws@eIL4YSTnGm">
        <value name="IF0">
          <block type="logic_compare" id="rA2gdIE]XmZZP.f#r.y}">
            <field name="OP">EQ</field>
            <value name="A">
              <block type="last_digit" id="~qBk-@f^k2$~cTw_O~lu"></block>
            </value>
            <value name="B">
              <block type="math_number" id="4-l`c/`.}_=##UoWupvT">
                <field name="NUM">1</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="notify" id="PP:LpsqGXW=k-{ZZmWEJ">
            <field name="NOTIFICATION_TYPE">info</field>
            <field name="NOTIFICATION_SOUND">earned-money</field>
            <value name="MESSAGE">
              <shadow type="text" id="tmhABSsIZ5TsRtLrl47E">
                <field name="TEXT">abc</field>
              </shadow>
              <block type="text" id="4-?5*k@6^:rx9P8A%`G@">
                <field name="TEXT">PLAY ON BOT</field>
              </block>
            </value>
            <next>
              <block type="purchase" id="W6q#Z-I3q3d[d3-`S[dS">
                <field name="PURCHASE_LIST">DIGITOVER</field>
              </block>
            </next>
          </block>
        </statement>
      </block>
    </statement>
  </block>
  <block type="tick_analysis" id="jP:vU]LS#wRxvo[VH4,C" collapsed="true" x="0" y="808">
    <statement name="TICKANALYSIS_STACK">
      <block type="controls_if" id="joWT)oGv%btN(WB(lA:^">
        <mutation elseif="1"></mutation>
        <value name="IF0">
          <block type="logic_operation" id="PvEeTdFyq?N:Jv3W[Aa[" inline="false">
            <field name="OP">AND</field>
            <value name="A">
              <block type="check_direction" id="aWxa`}{:iw1|gMJUL:5r">
                <field name="CHECK_DIRECTION">rise</field>
              </block>
            </value>
            <value name="B">
              <block type="logic_negate" id="N_.qwD{kotN9Z{mgib!D">
                <value name="BOOL">
                  <block type="is_candle_black" id="hC{j*:MTsza];QYTbNiE">
                    <value name="OHLCOBJ">
                      <block type="get_ohlc" id="._zQZ]glTjSpl,yzJ}zW">
                        <field name="CANDLEINTERVAL_LIST">default</field>
                        <value name="CANDLEINDEX">
                          <shadow type="math_number" id="sSeiY1Nv],beNJAGe~)(">
                            <field name="NUM">1</field>
                          </shadow>
                        </value>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="notify" id="%lH)+Zq,eHCn(PCV8,O?">
            <field name="NOTIFICATION_TYPE">info</field>
            <field name="NOTIFICATION_SOUND">silent</field>
            <value name="MESSAGE">
              <shadow type="text" id="gfqy?,1$@@%PTH_jS$*Q">
                <field name="TEXT">UP</field>
              </shadow>
              <block type="text_join" id="`n9%U+]bIj1gO%*,@LWh">
                <mutation items="3"></mutation>
                <value name="ADD0">
                  <block type="text" id="@)=-jet=Y)~%.-:N0i)C">
                    <field name="TEXT">UP : ▲</field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="text" id="DIm4CV=pA/@(Ql%;5e+,">
                    <field name="TEXT"> [] CANDLE HIJAU [] </field>
                  </block>
                </value>
                <value name="ADD2">
                  <block type="last_digit" id="hRx@3-znjKj$;C=3$%:%"></block>
                </value>
              </block>
            </value>
          </block>
        </statement>
        <value name="IF1">
          <block type="logic_operation" id="du0t[#=$Gw7N;M%!1~,7" inline="false">
            <field name="OP">AND</field>
            <value name="A">
              <block type="check_direction" id="r~A]4,4ixNqh^0wigIdS">
                <field name="CHECK_DIRECTION">fall</field>
              </block>
            </value>
            <value name="B">
              <block type="logic_negate" id="Fghz^0SjAm_f8:b`O)wg">
                <value name="BOOL">
                  <block type="is_candle_black" id="qq+)]6C|7Y4JMgx8Tfj+">
                    <value name="OHLCOBJ">
                      <block type="get_ohlc" id="FL1VveG.Q%40KL@bsLF9">
                        <field name="CANDLEINTERVAL_LIST">default</field>
                        <value name="CANDLEINDEX">
                          <shadow type="math_number" id="@JY{Cy_4p7xVW+*KKZe.">
                            <field name="NUM">1</field>
                          </shadow>
                        </value>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO1">
          <block type="notify" id="[oJGDr]jKXLzLyZew!Ip">
            <field name="NOTIFICATION_TYPE">error</field>
            <field name="NOTIFICATION_SOUND">silent</field>
            <value name="MESSAGE">
              <shadow type="text" id="_t7nF%a.%#49oOa,ZY]/">
                <field name="TEXT">DOWN</field>
              </shadow>
              <block type="text_join" id=",(YqkjOfg^8av)ny,[@D">
                <mutation items="3"></mutation>
                <value name="ADD0">
                  <block type="text" id="{^~}v.v%`FFgY4E95[#O">
                    <field name="TEXT">DOWN : ▼</field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="text" id="]uTOOHY=SC8iDy_32^y)">
                    <field name="TEXT"> [] CANDLE HIJAU [] </field>
                  </block>
                </value>
                <value name="ADD2">
                  <block type="last_digit" id="(_Z+JeRuEy%bYMbIpAVu"></block>
                </value>
              </block>
            </value>
          </block>
        </statement>
        <next>
          <block type="controls_if" id="_e0hsN%!;:oX*dY]X4.K">
            <mutation elseif="1"></mutation>
            <value name="IF0">
              <block type="logic_operation" id="U:Bf3jifwQR.54TwWg3y" inline="false">
                <field name="OP">AND</field>
                <value name="A">
                  <block type="check_direction" id="A$}bQ/:E-Ew4ktZ!R,jg">
                    <field name="CHECK_DIRECTION">rise</field>
                  </block>
                </value>
                <value name="B">
                  <block type="is_candle_black" id="22q{h;Zt-Z;SIm+~TRM%">
                    <value name="OHLCOBJ">
                      <block type="get_ohlc" id="r%9Hk34uzya{i4o.QBXJ">
                        <field name="CANDLEINTERVAL_LIST">default</field>
                        <value name="CANDLEINDEX">
                          <shadow type="math_number" id="e6O^$$Mgs7[|N~r4ol|J">
                            <field name="NUM">1</field>
                          </shadow>
                        </value>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO0">
              <block type="notify" id="?H/SOQ:5gXQqui^^*c4(">
                <field name="NOTIFICATION_TYPE">info</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="gfqy?,1$@@%PTH_jS$*Q">
                    <field name="TEXT">UP</field>
                  </shadow>
                  <block type="text_join" id="(h?B~RB*]I=!#-)UFXyv">
                    <mutation items="3"></mutation>
                    <value name="ADD0">
                      <block type="text" id="3zRb(2v`rj5SdZKYp#:K">
                        <field name="TEXT">UP : ▲</field>
                      </block>
                    </value>
                    <value name="ADD1">
                      <block type="text" id="=;UNrnhP.e^o+^V_*Dv-">
                        <field name="TEXT"> [] CANDLE MERAH [] </field>
                      </block>
                    </value>
                    <value name="ADD2">
                      <block type="last_digit" id="+@+_5`c)NhXird.qFD=!"></block>
                    </value>
                  </block>
                </value>
              </block>
            </statement>
            <value name="IF1">
              <block type="logic_operation" id="!s$#T;,d-CRWH^~umI/+" inline="false">
                <field name="OP">AND</field>
                <value name="A">
                  <block type="check_direction" id="~#Dmkb.~ii*[[@oP$p)R">
                    <field name="CHECK_DIRECTION">fall</field>
                  </block>
                </value>
                <value name="B">
                  <block type="is_candle_black" id="}`=I9gwZG=NMIQGB.B=:">
                    <value name="OHLCOBJ">
                      <block type="get_ohlc" id="v47rF^I$mYR%{4{-rZcw">
                        <field name="CANDLEINTERVAL_LIST">default</field>
                        <value name="CANDLEINDEX">
                          <shadow type="math_number" id="q%R@b@[Pkj?K{Sa4IR=y">
                            <field name="NUM">1</field>
                          </shadow>
                        </value>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO1">
              <block type="notify" id="mFljqZ6%?:)Loy1ZK6FD">
                <field name="NOTIFICATION_TYPE">error</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="_t7nF%a.%#49oOa,ZY]/">
                    <field name="TEXT">DOWN</field>
                  </shadow>
                  <block type="text_join" id="Hit5or#H$C4z%sx{c/Nk">
                    <mutation items="3"></mutation>
                    <value name="ADD0">
                      <block type="text" id="3dMZO|6g*a[0tEsr|p^4">
                        <field name="TEXT">DOWN : ▼</field>
                      </block>
                    </value>
                    <value name="ADD1">
                      <block type="text" id=".LToP`mR=[,CXoVb^vAW">
                        <field name="TEXT"> [] CANDLE MERAH [] </field>
                      </block>
                    </value>
                    <value name="ADD2">
                      <block type="last_digit" id="M2h~Y^}IjV3sdCfqmj.)"></block>
                    </value>
                  </block>
                </value>
              </block>
            </statement>
          </block>
        </next>
      </block>
    </statement>
  </block>
  <block type="after_purchase" id="D^Jz1^n=2vtZku1vBN@;" x="0" y="861">
    <statement name="AFTERPURCHASE_STACK">
      <block type="controls_if" id="MWfD@xu;F8=$W^m|3SAE">
        <mutation else="1"></mutation>
        <value name="IF0">
          <block type="contract_check_result" id="~we^R9BWKW?k[/q~}PEo">
            <field name="CHECK_RESULT">loss</field>
          </block>
        </value>
        <statement name="DO0">
          <block type="notify" id="A1C{t_TuE~UvZn#}.9^o">
            <field name="NOTIFICATION_TYPE">error</field>
            <field name="NOTIFICATION_SOUND">error</field>
            <value name="MESSAGE">
              <shadow type="text" id="%m~b19cIWsS7^vq.mw63">
                <field name="TEXT">KONDISI TREND SIDEWAY.!!  HENTIKAN BOT ATAU GANTI MARKET</field>
              </shadow>
              <block type="text_join" id="fR/vtn,bE0e^@l$V8GYi">
                <mutation items="3"></mutation>
                <value name="ADD0">
                  <block type="text" id="/Q~cr]_;lIG%exeR+GDW">
                    <field name="TEXT">LOST $ </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="math_single" id="~*}G:a@Jr0Lc_OkEa6PT">
                    <field name="OP">ABS</field>
                    <value name="NUM">
                      <shadow type="math_number" id="GleSn`9j7Cm7/dqg}FIA">
                        <field name="NUM">9</field>
                      </shadow>
                      <block type="read_details" id="`T=SI,$;QP.$1;l)f*@K">
                        <field name="DETAIL_INDEX">4</field>
                      </block>
                    </value>
                  </block>
                </value>
                <value name="ADD2">
                  <block type="text" id="^]Bk_K`Mlj=;d#j?nQ{#">
                    <field name="TEXT"> AJA [] </field>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="math_change" id="gPvEt}Pk-nZ,-C@.T;d;">
                <field name="VAR" id="nfN(I4pYa%!hdG-=ekrk" variabletype="">Initial Stake</field>
                <value name="DELTA">
                  <shadow type="math_number" id="5M3[cW:{%(wI5rvg~W/j">
                    <field name="NUM">1</field>
                  </shadow>
                  <block type="math_single" id="us)XCcy5?qg)ajF|d_cf">
                    <field name="OP">ABS</field>
                    <value name="NUM">
                      <shadow type="math_number" id="g`7h;}T)P@YAo2a{GF1N">
                        <field name="NUM">9</field>
                      </shadow>
                      <block type="math_arithmetic" id="}V_S-)x*lfl8#|atJ_mk">
                        <field name="OP">MULTIPLY</field>
                        <value name="A">
                          <shadow type="math_number" id=";,4DC`1|3=X7y@)cCq-`">
                            <field name="NUM">1</field>
                          </shadow>
                          <block type="read_details" id="Kp*mR?/`8QTIB(k)vi~I">
                            <field name="DETAIL_INDEX">4</field>
                          </block>
                        </value>
                        <value name="B">
                          <shadow type="math_number" id="iXqYk9o)sJ_=$mBKvUz!">
                            <field name="NUM">1.05</field>
                          </shadow>
                          <block type="variables_get" id=",663dU;xJ`%:r?S[P-+b">
                            <field name="VAR" id="WB^wGp{On}ZKq/4LK4Ca" variabletype="">MARTI</field>
                          </block>
                        </value>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </next>
          </block>
        </statement>
        <statement name="ELSE">
          <block type="notify" id="w7N#IlRarY,(Xo*6ct.a">
            <field name="NOTIFICATION_TYPE">info</field>
            <field name="NOTIFICATION_SOUND">earned-money</field>
            <value name="MESSAGE">
              <shadow type="text" id="%CVs|4Gu8q12EK~Ipf^/">
                <field name="TEXT">KONDISI TREND SIDEWAY.!!  HENTIKAN BOT ATAU GANTI MARKET</field>
              </shadow>
              <block type="text_join" id="UW:t77Ffa5!Fa}bBYivz">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id="M}+xpZx`OkTQL,KEvr{o">
                    <field name="TEXT">ALHAMDULILLAH PROFIT = $ </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="read_details" id="EX7nWxp9L6FB@Q!)~f{t">
                    <field name="DETAIL_INDEX">4</field>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="variables_set" id="KmW5t5vChmNlj*O%:[^H">
                <field name="VAR" id="nfN(I4pYa%!hdG-=ekrk" variabletype="">Initial Stake</field>
                <value name="VALUE">
                  <block type="variables_get" id="ccnQ7l$BRa^/{;,{x~a#">
                    <field name="VAR" id="/|o~W%gQIAM#UHZO!zA*" variabletype="">STAKE_MODAL</field>
                  </block>
                </value>
              </block>
            </next>
          </block>
        </statement>
        <next>
          <block type="controls_if" id="x]wtt#@8_5_u97!zaI?M">
            <mutation elseif="1" else="1"></mutation>
            <value name="IF0">
              <block type="logic_operation" id="9jpE.-|$Ne$(|QX-X7Ja">
                <field name="OP">AND</field>
                <value name="A">
                  <block type="math_number_property" id="yW1^m!z(h%;m}Vfe#r@^">
                    <mutation divisor_input="false"></mutation>
                    <field name="PROPERTY">NEGATIVE</field>
                    <value name="NUMBER_TO_CHECK">
                      <shadow type="math_number" id="2TJ^lPjT8MrR^:6Ghug=">
                        <field name="NUM">0</field>
                      </shadow>
                      <block type="total_profit" id="uqlDU#QMdm-s]jyv]$B#"></block>
                    </value>
                  </block>
                </value>
                <value name="B">
                  <block type="logic_compare" id="mrZXmIf1M3D#D?y=JbT?">
                    <field name="OP">GTE</field>
                    <value name="A">
                      <block type="math_single" id="H^KAC0A$VO^a:/J[+q}g">
                        <field name="OP">ABS</field>
                        <value name="NUM">
                          <shadow type="math_number" id="(rCiW:kP-Kx+n[/lS.n{">
                            <field name="NUM">9</field>
                          </shadow>
                          <block type="total_profit" id="G[25$kY~T~gCVfYR+0gT"></block>
                        </value>
                      </block>
                    </value>
                    <value name="B">
                      <block type="variables_get" id="kMaqW~2,vwv=ESaSZV8W">
                        <field name="VAR" id="+e9-IVuJ/mv#4%/,MX2r" variabletype="">STOP_LOSS</field>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO0">
              <block type="text_print" id="!7NiL,!:A+26$;ddTQA%">
                <value name="TEXT">
                  <shadow type="text" id="eZUb-P^OKXwOD]NR4c~?">
                    <field name="TEXT">abc</field>
                  </shadow>
                  <block type="text_join" id="jG4QhkVO0H8aQJR6$Fbn">
                    <mutation items="2"></mutation>
                    <value name="ADD0">
                      <block type="text" id="wGDOy/6|[~/y+DEgUVyd">
                        <field name="TEXT">Loss!! No Problem</field>
                      </block>
                    </value>
                    <value name="ADD1">
                      <block type="math_single" id="qp)ri$iTf|.Fv#7_0r=E">
                        <field name="OP">ABS</field>
                        <value name="NUM">
                          <shadow type="math_number" id="(rCiW:kP-Kx+n[/lS.n{">
                            <field name="NUM">9</field>
                          </shadow>
                          <block type="total_profit" id="s}QwbK*GYx/qP9=:,v%!"></block>
                        </value>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </statement>
            <value name="IF1">
              <block type="logic_compare" id="09xbI)b?+bZ_($~oM`g0">
                <field name="OP">GTE</field>
                <value name="A">
                  <block type="total_profit" id="p0)!Pu);zW*:$OwI.GdH"></block>
                </value>
                <value name="B">
                  <block type="variables_get" id="KE^;=^{}E#+]0^1PG,$P">
                    <field name="VAR" id="3C@HUF)?z(zn8g3GPaNd" variabletype="">TARGET PROFIT</field>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO1">
              <block type="text_print" id="kS:0E.8[k#l_,ofl;r5.">
                <value name="TEXT">
                  <shadow type="text" id="eZUb-P^OKXwOD]NR4c~?">
                    <field name="TEXT">abc</field>
                  </shadow>
                  <block type="text_join" id="+Wa/G#bE=`+DK0;,_ZBN">
                    <mutation items="3"></mutation>
                    <value name="ADD0">
                      <block type="text" id="2_j]n=}b*JXgR/_Y1TA{">
                        <field name="TEXT">Asik M-POK Kecolong $ </field>
                      </block>
                    </value>
                    <value name="ADD1">
                      <block type="total_profit" id="!NQxO^Z;IMww7*=pdEz2"></block>
                    </value>
                    <value name="ADD2">
                      <block type="text" id=":NO!.*]]4msA1T34q;FB">
                        <field name="TEXT"> USD</field>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </statement>
            <statement name="ELSE">
              <block type="controls_if" id=";E5?xIr$8!?F8Hs41kDm">
                <value name="IF0">
                  <block type="logic_compare" id="D9bEjC8I~.vz_N9lH{T0">
                    <field name="OP">LT</field>
                    <value name="A">
                      <block type="total_profit" id="=eQm2XSw.rYyExEUXjVr"></block>
                    </value>
                    <value name="B">
                      <block type="variables_get" id="ig@yG0`jyxWH6QP!$R|z">
                        <field name="VAR" id="3C@HUF)?z(zn8g3GPaNd" variabletype="">TARGET PROFIT</field>
                      </block>
                    </value>
                  </block>
                </value>
                <statement name="DO0">
                  <block type="trade_again" id="4@JcI#uIDv~c(PPGio_`"></block>
                </statement>
              </block>
            </statement>
          </block>
        </next>
      </block>
    </statement>
  </block>
</xml> 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Shoun22/Shoun22 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
