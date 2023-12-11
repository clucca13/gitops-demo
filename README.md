
package pipeline_environment


deny[sprintf("Scan can't contain any critical vulnerability '%s'", [input.PRISMACLOUD_NEWCRITICAL])] {
    input.PRISMACLOUD_NEWCRITICAL != 0
}







package pipeline_environment


deny[sprintf("Scan can't contain any critical vulnerability '%s'", [input.VERACODE_NEWCRITICAL])] {
    input.VERACODE_NEWCRITICAL != 0
}






{“PRISMACLOUD_NEWCRITICAL”:<+pipeline.stages.sq.spec.execution.steps.PrismaCloud_1.output.outputVariables.NEW_CRITICAL>,“VERACODE_NEWCRITICAL": <+pipeline.stages.sq.spec.execution.steps.Veracode.output.outputVariables.NEW_CRITICAL>}
