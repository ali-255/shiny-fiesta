# shiny-fiesta

trash repo

this was added for trash purposes

*** Assertion failure in -[UITableView _dequeueReusableCellWithIdentifier:forIndexPath:usingPresentationValues:], UITableView.m:10108
*** Terminating app due to uncaught exception 'NSInternalInconsistencyException', reason: 'unable to dequeue a cell with identifier TechnicianCardCell - must register a nib or a class for the identifier or connect a prototype cell in a storyboard'
*** First throw call stack:
(
	0   CoreFoundation                      0x00000001804c9690 __exceptionPreprocess + 172
	1   libobjc.A.dylib                     0x00000001800937cc objc_exception_throw + 72
	2   Foundation                          0x0000000180e54db4 _userInfoForFileAndLine + 0
	3   UIKitCore                           0x0000000185ea2f20 -[UITableView _dequeueReusableCellWithIdentifier:forIndexPath:usingPresentationValues:] + 748
	4   UIKitCore                           0x0000000185ea2c10 -[UITableView dequeueReusableCellWithIdentifier:forIndexPath:] + 68
	5   PolyTech.debug.dylib                0x000000010495efe8 $s8PolyTech25TechniciansViewControllerC05tableD0_12cellForRowAtSo07UITableD4CellCSo0kD0C_10Foundation9IndexPathVtF + 324
	6   PolyTech.debug.dylib                0x000000010495fd58 $s8PolyTech25TechniciansViewControllerC05tableD0_12cellForRowAtSo07UITableD4CellCSo0kD0C_10Foundation9IndexPathVtFTo + 160
	7   UIKitCore                           0x0000000185eb81ac -[UITableView _createPreparedCellForGlobalRow:withIndexPath:willDisplay:] + 1376
	8   UIKitCore                           0x0000000185e8a64c -[UITableView _updateVisibleCellsForRanges:createIfNecessary:] + 540
	9   UIKitCore                           0x0000000185e8ac40 -[UITableView _updateVisibleCellsNow:] + 1100
	10  UIKitCore                           0x0000000185ea5348 -[UITableView layoutSubviews] + 144
	11  UIKitCore                           0x00000001861d35e0 -[UIView(CALayerDelegate) layoutSublayersOfLayer:] + 2420
	12  QuartzCore                          0x000000018b5939a0 _ZN2CA5Layer16layout_if_neededEPNS_11TransactionE + 424
	13  QuartzCore                          0x000000018b59ea70 _ZN2CA5Layer28layout_and_display_if_neededEPNS_11TransactionE + 132
	14  QuartzCore                          0x000000018b4cca30 _ZN2CA7Context18commit_transactionEPNS_11TransactionEdPd + 484
	15  QuartzCore                          0x000000018b4fb684 _ZN2CA11Transaction6commitEv + 636
	16  UIKitCore                           0x0000000185c779a8 __34-[UIApplication _firstCommitBlock]_block_invoke_2 + 32
	17  CoreFoundation                      0x0000000180428fe0 __CFRUNLOOP_IS_CALLING_OUT_TO_A_BLOCK__ + 20
	18  CoreFoundation                      0x0000000180428744 __CFRunLoopDoBlocks + 348
	19  CoreFoundation                      0x00000001804232fc __CFRunLoopRun + 808
	20  CoreFoundation                      0x0000000180422b98 CFRunLoopRunSpecific + 536
	21  GraphicsServices                    0x000000019101fd00 GSEventRunModal + 164
	22  UIKitCore                           0x0000000185c5ebb8 -[UIApplication _run] + 796
	23  UIKitCore                           0x0000000185c62f84 UIApplicationMain + 124
	24  UIKitCore                           0x0000000185028f88 block_destroy_helper.14 + 9560
	25  PolyTech.debug.dylib                0x000000010497431c $sSo21UIApplicationDelegateP5UIKitE4mainyyFZ + 128
	26  PolyTech.debug.dylib                0x000000010497428c $s8PolyTech11AppDelegateC5$mainyyFZ + 44
	27  PolyTech.debug.dylib                0x0000000104974398 __debug_main_executable_dylib_entry_point + 28
	28  dyld                                0x0000000102dc13d4 start_sim + 20
	29  ???                                 0x0000000103026274 0x0 + 4345455220
	30  ???                                 0x7518800000000000 0x0 + 8437634639366979584
)
libc++abi: terminating due to uncaught exception of type NSException
