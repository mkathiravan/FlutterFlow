<img width="1728" alt="Screenshot 2024-10-21 at 10 07 04 PM" src="https://github.com/user-attachments/assets/ff99e7ae-e29b-40b4-85e7-95c2c8b71b67">

<img width="1176" alt="Screenshot 2024-10-21 at 10 09 02 PM" src="https://github.com/user-attachments/assets/dfee2cad-6714-421b-ae69-70cdc238bf57">


<img width="1254" alt="Screenshot 2024-10-21 at 10 12 11 PM" src="https://github.com/user-attachments/assets/63f52254-a869-4ea0-9590-67b3be2c9bc9">


<img width="412" alt="Screenshot 2024-10-21 at 10 17 41 PM" src="https://github.com/user-attachments/assets/a7de5837-6fe3-4d72-8a81-0d75f71264fa">

<img width="365" alt="Screenshot 2024-10-21 at 10 18 16 PM" src="https://github.com/user-attachments/assets/1c940807-1640-461f-b1ca-889a32feba4b">






                  import '/flutter_flow/flutter_flow_theme.dart';
                  import '/flutter_flow/flutter_flow_util.dart';
                  import '/flutter_flow/flutter_flow_widgets.dart';
                  import 'package:flutter/material.dart';
                  import 'package:google_fonts/google_fonts.dart';
                  import 'package:provider/provider.dart';
                  
                  import 'home_page_model.dart';
                  export 'home_page_model.dart';
                  
                  class HomePageWidget extends StatefulWidget {
                    const HomePageWidget({super.key});
                  
                    @override
                    State<HomePageWidget> createState() => _HomePageWidgetState();
                  }
                  
                  class _HomePageWidgetState extends State<HomePageWidget> {
                    late HomePageModel _model;
                  
                    final scaffoldKey = GlobalKey<ScaffoldState>();
                  
                    @override
                    void initState() {
                      super.initState();
                      _model = createModel(context, () => HomePageModel());
                  
                      _model.usernameTextController ??= TextEditingController();
                      _model.usernameFocusNode ??= FocusNode();
                  
                      _model.passwordTextController ??= TextEditingController();
                      _model.passwordFocusNode ??= FocusNode();
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
                          body: SafeArea(
                            top: true,
                            child: Column(
                              mainAxisSize: MainAxisSize.max,
                              mainAxisAlignment: MainAxisAlignment.start,
                              crossAxisAlignment: CrossAxisAlignment.start,
                              children: [
                                Form(
                                  key: _model.formKey,
                                  autovalidateMode: AutovalidateMode.disabled,
                                  child: Column(
                                    mainAxisSize: MainAxisSize.max,
                                    children: [
                                      Padding(
                                        padding: EdgeInsetsDirectional.fromSTEB(10, 0, 10, 0),
                                        child: Container(
                                          width: 400,
                                          child: TextFormField(
                                            controller: _model.usernameTextController,
                                            focusNode: _model.usernameFocusNode,
                                            autofocus: false,
                                            obscureText: false,
                                            decoration: InputDecoration(
                                              isDense: true,
                                              labelStyle: FlutterFlowTheme.of(context)
                                                  .labelMedium
                                                  .override(
                                                    fontFamily: 'Inter',
                                                    letterSpacing: 0.0,
                                                  ),
                                              hintText: 'Enter user name',
                                              hintStyle: FlutterFlowTheme.of(context)
                                                  .labelMedium
                                                  .override(
                                                    fontFamily: 'Inter',
                                                    letterSpacing: 0.0,
                                                  ),
                                              enabledBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: Color(0x00000000),
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              focusedBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: Color(0x00000000),
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              errorBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: FlutterFlowTheme.of(context).error,
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              focusedErrorBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: FlutterFlowTheme.of(context).error,
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              filled: true,
                                              fillColor: FlutterFlowTheme.of(context)
                                                  .secondaryBackground,
                                            ),
                                            style:
                                                FlutterFlowTheme.of(context).bodyMedium.override(
                                                      fontFamily: 'Inter',
                                                      letterSpacing: 0.0,
                                                    ),
                                            cursorColor: FlutterFlowTheme.of(context).primaryText,
                                            validator: _model.usernameTextControllerValidator
                                                .asValidator(context),
                                          ),
                                        ),
                                      ),
                                      Padding(
                                        padding: EdgeInsets.all(12),
                                        child: Container(
                                          width: 400,
                                          child: TextFormField(
                                            controller: _model.passwordTextController,
                                            focusNode: _model.passwordFocusNode,
                                            autofocus: false,
                                            obscureText: !_model.passwordVisibility,
                                            decoration: InputDecoration(
                                              isDense: true,
                                              labelStyle: FlutterFlowTheme.of(context)
                                                  .labelMedium
                                                  .override(
                                                    fontFamily: 'Inter',
                                                    letterSpacing: 0.0,
                                                  ),
                                              hintText: 'Enter your password',
                                              hintStyle: FlutterFlowTheme.of(context)
                                                  .labelMedium
                                                  .override(
                                                    fontFamily: 'Inter',
                                                    letterSpacing: 0.0,
                                                  ),
                                              enabledBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: Color(0x00000000),
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              focusedBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: Color(0x00000000),
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              errorBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: FlutterFlowTheme.of(context).error,
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              focusedErrorBorder: OutlineInputBorder(
                                                borderSide: BorderSide(
                                                  color: FlutterFlowTheme.of(context).error,
                                                  width: 1,
                                                ),
                                                borderRadius: BorderRadius.circular(8),
                                              ),
                                              filled: true,
                                              fillColor: FlutterFlowTheme.of(context)
                                                  .secondaryBackground,
                                              suffixIcon: InkWell(
                                                onTap: () => safeSetState(
                                                  () => _model.passwordVisibility =
                                                      !_model.passwordVisibility,
                                                ),
                                                focusNode: FocusNode(skipTraversal: true),
                                                child: Icon(
                                                  _model.passwordVisibility
                                                      ? Icons.visibility_outlined
                                                      : Icons.visibility_off_outlined,
                                                  size: 20,
                                                ),
                                              ),
                                            ),
                                            style:
                                                FlutterFlowTheme.of(context).bodyMedium.override(
                                                      fontFamily: 'Inter',
                                                      letterSpacing: 0.0,
                                                    ),
                                            cursorColor: FlutterFlowTheme.of(context).primaryText,
                                            validator: _model.passwordTextControllerValidator
                                                .asValidator(context),
                                          ),
                                        ),
                                      ),
                                      Padding(
                                        padding: EdgeInsetsDirectional.fromSTEB(0, 20, 0, 0),
                                        child: FFButtonWidget(
                                          onPressed: () async {
                                            if (_model.formKey.currentState == null ||
                                                !_model.formKey.currentState!.validate()) {
                                              return;
                                            }
                                          },
                                          text: 'Submit',
                                          options: FFButtonOptions(
                                            height: 40,
                                            padding: EdgeInsetsDirectional.fromSTEB(16, 0, 16, 0),
                                            iconPadding:
                                                EdgeInsetsDirectional.fromSTEB(0, 0, 0, 0),
                                            color: FlutterFlowTheme.of(context).primary,
                                            textStyle:
                                                FlutterFlowTheme.of(context).titleSmall.override(
                                                      fontFamily: 'Inter Tight',
                                                      color: Colors.white,
                                                      letterSpacing: 0.0,
                                                    ),
                                            elevation: 0,
                                            borderRadius: BorderRadius.circular(8),
                                          ),
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




### HomePage Model


          import '/flutter_flow/flutter_flow_theme.dart';
          import '/flutter_flow/flutter_flow_util.dart';
          import '/flutter_flow/flutter_flow_widgets.dart';
          import 'home_page_widget.dart' show HomePageWidget;
          import 'package:flutter/material.dart';
          import 'package:google_fonts/google_fonts.dart';
          import 'package:provider/provider.dart';
          
          class HomePageModel extends FlutterFlowModel<HomePageWidget> {
            ///  State fields for stateful widgets in this page.
          
            final formKey = GlobalKey<FormState>();
            // State field(s) for username widget.
            FocusNode? usernameFocusNode;
            TextEditingController? usernameTextController;
            String? Function(BuildContext, String?)? usernameTextControllerValidator;
            String? _usernameTextControllerValidator(BuildContext context, String? val) {
              if (val == null || val.isEmpty) {
                return 'Field is required';
              }
          
              if (val.length < 4) {
                return 'enter your valid name';
              }
          
              return null;
            }
          
            // State field(s) for password widget.
            FocusNode? passwordFocusNode;
            TextEditingController? passwordTextController;
            late bool passwordVisibility;
            String? Function(BuildContext, String?)? passwordTextControllerValidator;
            String? _passwordTextControllerValidator(BuildContext context, String? val) {
              if (val == null || val.isEmpty) {
                return 'Field is required';
              }
          
              if (val.length < 8) {
                return 'enter a valid password';
              }
          
              return null;
            }
          
            @override
            void initState(BuildContext context) {
              usernameTextControllerValidator = _usernameTextControllerValidator;
              passwordVisibility = false;
              passwordTextControllerValidator = _passwordTextControllerValidator;
            }
          
            @override
            void dispose() {
              usernameFocusNode?.dispose();
              usernameTextController?.dispose();
          
              passwordFocusNode?.dispose();
              passwordTextController?.dispose();
            }
          }

