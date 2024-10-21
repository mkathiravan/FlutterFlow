<img width="1711" alt="Screenshot 2024-10-21 at 8 47 11 PM" src="https://github.com/user-attachments/assets/2921c4b0-b1c8-48f0-b60e-7651990555e1">

<img width="1727" alt="Screenshot 2024-10-21 at 8 47 00 PM" src="https://github.com/user-attachments/assets/2a43d387-b8fc-4f7f-bb32-b1bc41bb960d">



              import '/flutter_flow/flutter_flow_button_tabbar.dart';
              import '/flutter_flow/flutter_flow_icon_button.dart';
              import '/flutter_flow/flutter_flow_theme.dart';
              import '/flutter_flow/flutter_flow_util.dart';
              import '/flutter_flow/flutter_flow_widgets.dart';
              import 'package:flutter/material.dart';
              import 'package:font_awesome_flutter/font_awesome_flutter.dart';
              import 'package:google_fonts/google_fonts.dart';
              import 'package:provider/provider.dart';
              
              import 'home_page_model.dart';
              export 'home_page_model.dart';
              
              class HomePageWidget extends StatefulWidget {
                const HomePageWidget({super.key});
              
                @override
                State<HomePageWidget> createState() => _HomePageWidgetState();
              }
              
              class _HomePageWidgetState extends State<HomePageWidget>
                  with TickerProviderStateMixin {
                late HomePageModel _model;
              
                final scaffoldKey = GlobalKey<ScaffoldState>();
              
                @override
                void initState() {
                  super.initState();
                  _model = createModel(context, () => HomePageModel());
              
                  _model.tabBarController = TabController(
                    vsync: this,
                    length: 3,
                    initialIndex: 0,
                  )..addListener(() => safeSetState(() {}));
                }
              
                @override
                void dispose() {
                  _model.dispose();
              
                  super.dispose();
                }
              
                @override
                Widget build(BuildContext context) {
                  return GestureDetector(
                    onTap: () => FocusScope.of(context).unfocus(),
                    child: Scaffold(
                      key: scaffoldKey,
                      backgroundColor: FlutterFlowTheme.of(context).primaryBackground,
                      appBar: AppBar(
                        backgroundColor: FlutterFlowTheme.of(context).primary,
                        automaticallyImplyLeading: false,
                        leading: FlutterFlowIconButton(
                          borderColor: Colors.transparent,
                          borderRadius: 30,
                          borderWidth: 1,
                          buttonSize: 60,
                          icon: Icon(
                            Icons.arrow_back_rounded,
                            color: Colors.white,
                            size: 30,
                          ),
                          onPressed: () async {
                            context.pop();
                          },
                        ),
                        title: Text(
                          'Page Title',
                          style: FlutterFlowTheme.of(context).headlineMedium.override(
                                fontFamily: 'Inter Tight',
                                color: Colors.white,
                                fontSize: 22,
                                letterSpacing: 0.0,
                              ),
                        ),
                        actions: [],
                        centerTitle: false,
                        elevation: 2,
                      ),
                      body: SafeArea(
                        top: true,
                        child: Column(
                          mainAxisSize: MainAxisSize.max,
                          children: [
                            Expanded(
                              child: Column(
                                children: [
                                  Align(
                                    alignment: Alignment(0, 0),
                                    child: FlutterFlowButtonTabBar(
                                      useToggleButtonStyle: false,
                                      labelStyle:
                                          FlutterFlowTheme.of(context).titleMedium.override(
                                                fontFamily: 'Inter Tight',
                                                letterSpacing: 0.0,
                                              ),
                                      unselectedLabelStyle:
                                          FlutterFlowTheme.of(context).titleMedium.override(
                                                fontFamily: 'Inter Tight',
                                                letterSpacing: 0.0,
                                              ),
                                      labelColor: FlutterFlowTheme.of(context).primaryText,
                                      unselectedLabelColor:
                                          FlutterFlowTheme.of(context).secondaryText,
                                      backgroundColor: FlutterFlowTheme.of(context).accent1,
                                      unselectedBackgroundColor:
                                          FlutterFlowTheme.of(context).alternate,
                                      borderColor: FlutterFlowTheme.of(context).primary,
                                      unselectedBorderColor:
                                          FlutterFlowTheme.of(context).alternate,
                                      borderWidth: 2,
                                      borderRadius: 8,
                                      elevation: 0,
                                      buttonMargin:
                                          EdgeInsetsDirectional.fromSTEB(8, 0, 8, 0),
                                      tabs: [
                                        Row(
                                          mainAxisAlignment: MainAxisAlignment.center,
                                          children: [
                                            FaIcon(
                                              FontAwesomeIcons.plane,
                                            ),
                                            Tab(
                                              text: 'Flight',
                                            ),
                                          ],
                                        ),
                                        Row(
                                          mainAxisAlignment: MainAxisAlignment.center,
                                          children: [
                                            FaIcon(
                                              FontAwesomeIcons.train,
                                            ),
                                            Tab(
                                              text: 'Train',
                                            ),
                                          ],
                                        ),
                                        Row(
                                          mainAxisAlignment: MainAxisAlignment.center,
                                          children: [
                                            FaIcon(
                                              FontAwesomeIcons.bus,
                                            ),
                                            Tab(
                                              text: 'Bus',
                                            ),
                                          ],
                                        ),
                                      ],
                                      controller: _model.tabBarController,
                                      onTap: (i) async {
                                        [() async {}, () async {}, () async {}][i]();
                                      },
                                    ),
                                  ),
                                  Expanded(
                                    child: TabBarView(
                                      controller: _model.tabBarController,
                                      children: [
                                        Container(
                                          width: 100,
                                          height: 100,
                                          decoration: BoxDecoration(
                                            color: FlutterFlowTheme.of(context)
                                                .secondaryBackground,
                                          ),
                                          child: ClipRRect(
                                            borderRadius: BorderRadius.circular(8),
                                            child: Image.asset(
                                              'assets/images/istockphoto-155439315-612x612.jpg',
                                              width: 200,
                                              height: 200,
                                              fit: BoxFit.fill,
                                            ),
                                          ),
                                        ),
                                        Container(
                                          width: 100,
                                          height: 100,
                                          decoration: BoxDecoration(
                                            color: FlutterFlowTheme.of(context)
                                                .secondaryBackground,
                                          ),
                                          child: ClipRRect(
                                            borderRadius: BorderRadius.circular(8),
                                            child: Image.asset(
                                              'assets/images/istockphoto-1278345107-612x612.jpg',
                                              width: 200,
                                              height: 200,
                                              fit: BoxFit.cover,
                                            ),
                                          ),
                                        ),
                                        Container(
                                          width: 100,
                                          height: 100,
                                          decoration: BoxDecoration(
                                            color: FlutterFlowTheme.of(context)
                                                .secondaryBackground,
                                          ),
                                          child: ClipRRect(
                                            borderRadius: BorderRadius.circular(8),
                                            child: Image.asset(
                                              'assets/images/ES4KE5bX0AA7IXI.jpg',
                                              width: 200,
                                              height: 200,
                                              fit: BoxFit.fill,
                                            ),
                                          ),
                                        ),
                                      ],
                                    ),
                                  ),
                                ],
                              ),
                            ),
                          ],
                        ),
                      ),
                    ),
                  );
                }
              }



  ### Model class
  
            import '/flutter_flow/flutter_flow_button_tabbar.dart';
            import '/flutter_flow/flutter_flow_icon_button.dart';
            import '/flutter_flow/flutter_flow_theme.dart';
            import '/flutter_flow/flutter_flow_util.dart';
            import '/flutter_flow/flutter_flow_widgets.dart';
            import 'home_page_widget.dart' show HomePageWidget;
            import 'package:flutter/material.dart';
            import 'package:font_awesome_flutter/font_awesome_flutter.dart';
            import 'package:google_fonts/google_fonts.dart';
            import 'package:provider/provider.dart';
            
            class HomePageModel extends FlutterFlowModel<HomePageWidget> {
              ///  State fields for stateful widgets in this page.
            
              // State field(s) for TabBar widget.
              TabController? tabBarController;
              int get tabBarCurrentIndex =>
                  tabBarController != null ? tabBarController!.index : 0;
            
              @override
              void initState(BuildContext context) {}
            
              @override
              void dispose() {
                tabBarController?.dispose();
              }
            }
