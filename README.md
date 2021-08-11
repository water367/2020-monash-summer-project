# 2020-monash-summer-project

this project is under supervision of Dr. Khalajzadeh &amp; Dr. Obie in monash university

# Detecting values-violating defects in source code (mobile apps)


### program structure

#### 1. animation

Animation API/hedonism value violation detector

	INPUT:JavaPath java file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	ViolationList ← an empty list
	VarNames ← an empty list
	for all AstNode in AstNodes do
		if AstNode is Variable Decelerator Nodethen
			if "Animator" inAstN ode.name then
				append AstNode.name to VarNames
			end if
		end if
		if AstNode is Method Invocation Node and AstNode.qualifier in VarNames then
			if AstNode.member ="setDuration" then
				for argument in AstNode.arguements do
					if argument.member > 2000 then
						append "Violation" to ViolationList
					end if
				end for
			end if
			if AstNode.member = "setRepeatCount" then
				for argument in AstNode.arguements do
					if argument.member = "Infinity" then
						append "Violation" in V iolationList
					end if
				end for
			end if
		end if
	end for
	for allListElement in ViolationList do
		if ListElement = "Violation" then
			Return True
		end if
	end for
	Return False





#### 2. hardware

Hardware API/Security value violation detector

	INPUT:JavaP athjava file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	ViolationList ← an empty list
	VarNames ← an empty list
	for all AstNode in AstNodes do
		if AstNode is VariableDeceleratorNode then
			if "Camera" = AstNode.name and "CameraDevice" = AstNode.namethen
				append AstNode.name to VarNames
			end if
		end if
		if AstNode is MethodInvocationNode and AstNode.qualifier in VarNames then
			if AstNode.member = "takePicture"or AstNode.member = "createCaptureSession" then
				append "Violation" in ViolationList
			end if
		end if
	end for
	for all ListElement in ViolationList do
		if ListElement = "Violation" then
			Return True
		end if
	end for
	Return False



#### 3. media

Media API/Universalism value violation detector

	INPUT:JavaPath java file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	ViolationList ← an empty list
	VarNames ← an empty list
	
	for all AstNode in AstNodes do
		if AstNode is Import Decelerator Node then
			if "com.google.android.exoplayer"=AstNode.paththen
				append "Violation" in ViolationList
			end if
		end if
	end for

	for all ListElement in ViolationList do
		if ListElement = "Violation" then
			ReturnTrue	
		end if
	end for

	Return False

Media API/self direction and hedonism value violation detector

	INPUT:JavaPath java file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	/*names of methods which we want to collect about mediaplaying and stop*/
	MethodIdentifyList ← an empty list
	/*names of methods categorized by different object whichwe collected in java file*/
	MethodDict ← an empty dictionary
	VarN ames ← an empty list
	for all AstN ode in AstN odes do
		if AstN ode is Variable Decelerator Node then
			if "MediaPlayer" = AstNode.name then
				append AstNode.nametoVar N ames
			end if
		end if
		if AstNode.member in MethodIdentifyList and AstNode.qualifier in VarNames then 
			append AstNode.member to MethodDict[AstNode.member]
		end if
	end for
	if MethodDict have mediaplay functions but not stop functions for all MediaPlayer objectthen
		Return True
	end if
	Return False



#### 4. mtp

Mtp API/self direction value violation detector

	INPUT:JavaP athjava file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	/*names of methods which we want to collect about datatransmission*/
	MethodIdentifyList ← an empty list
	/*names of methods which we collected in java file*/
	MethodList ← an empty list
	VarNames ← an empty list
	for all AstNode in AstNodes do
		if AstNode is VariableDeceleratorNode then
			if "MtpDevice" = AstNode.namethen
				append AstNode.nameto VarNames
			end if
		end if
		if AstNode.member in MethodIdentifyList and AstNode.qualifier in VarNames then
			append AstNode.member to MethodList
		end if
	end for
	if MethodList have data transmission function with only one direction then
		Return True
	end if
	Return False


#### 5. nfc

Nfc API/security value violation detector


	INPUT:JavaP athjava file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	ViolationList ← an empty list
	VarNames ← an empty list
	for all AstNode in AstNodes do
		if AstNode is VariableDeceleratorNode then
			if "Ndef" = AstNode.name then
				append AstNode.name to VarNames
			end if
		end if
		if AstNode is MethodInvocationNode and AstNode.qualifier in VarNames then
			if AstNode.member = "writeNdefMessage" then
				append AstNode.member in MethodInovationList
				if AstNode.member = "createApplicationRecord" then
					append AstNode.member in MethodInovationList
				end if
			end if
		end if
	end for
	if MethodInovationList includes "createApplication-Record" and "writeNdefMessage" then
		Return True
	end if
	Return False


#### 6. telephony

Telephony API/conformity value violation detector

	INPUT:JavaP athjava file path
	OUTPUT:return a boolean value:
		True: violation exist
		False: violation does not exist

	/*using deep first search to search all the AST nodes out*/
	AstNodes ← search(JavaPath)
	ViolationList ← an empty list
	VarNames ← an empty list
	for all AstNode in AstNodes do
		if AstNode is VariableDeceleratorNode then
			if "SmsManager" = AstNode.name then
				append AstNode.name to VarNames
			end if
		end if
		if AstNode is Method Invocation Node and AstNode.qualifier in VarNames then
			if AstNode.member is message sending function name then
				append”Violation”in V iolationList
			end if
		end if
	end for
	for all ListElement in ViolationList do
		if ListElement = "Violation" then
			Return True
		end if
	end for
	Return False


