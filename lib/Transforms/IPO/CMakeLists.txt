add_llvm_library(LLVMipo
  ArgumentPromotion.cpp
  BarrierNoopPass.cpp
  ConstantMerge.cpp
  DeadArgumentElimination.cpp
  ExtractGV.cpp
  FunctionAttrs.cpp
  GlobalDCE.cpp
  GlobalOpt.cpp
  IPConstantPropagation.cpp
  IPO.cpp
  InlineAlways.cpp
  InlineSimple.cpp
  Inliner.cpp
  Internalize.cpp
  LoopExtractor.cpp
  LowerBitSets.cpp
  MergeFunctions.cpp
  PartialInlining.cpp
  PassManagerBuilder.cpp
  PruneEH.cpp
  StripDeadPrototypes.cpp
  StripSymbols.cpp
  #SafeDispatch files:
  SafeDispatchCHA.cpp
  SafeDispatchFix.cpp
  SafeDispatchLayoutBuilder.cpp
  SafeDispatchMoveBasicBlocks.cpp
  SafeDispatchReturnAddressPass.cpp
  SafeDispatchReturnChecks.cpp
  SafeDispatchReturnRange.cpp
  SafeDispatchUpdateIndices.cpp
  SafeDispatchCleanup.cpp

  ADDITIONAL_HEADER_DIRS
  ${LLVM_MAIN_INCLUDE_DIR}/llvm/Transforms
  ${LLVM_MAIN_INCLUDE_DIR}/llvm/Transforms/IPO
  )

add_dependencies(LLVMipo intrinsics_gen)
