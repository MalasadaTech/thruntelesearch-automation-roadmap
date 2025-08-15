# thruntellisearch-automation-roadmap
## Basic info

This is just a placeholder to document stuff I'm working on. I've created an initial version for most of the stuff below. I've listed the processes that I perform regularly (or planned to implement like hIGMA) in my MalasadaTech hobbyist role. The end-state would be a system that automates myself out of my MalasadaTech Thruntellisearch role.

## Thringestor - https://github.com/MalasadaTech/Thringestor

A tool to automate thrintel ingestion (thringestion). The concept is to ingest from a source like Proofpoint's ET rules by checking a daily diff, creating a group by similar count (like when there's 10 lumma IOCs in one day), adding the list to a queue for processing. Another example could be something like pulling lumma indicators from threatfox, using threatfox-checker, on a daily basis, and then sending the outputs to IOC-comparer. 

In addition to collecting indicators from IOC aggregation sources, it should include an automated method to use agentic AI, with internet searching capabilities, to find user specified CTI. An example would be prompting an AI "Find me all blogs on SocGholish that were posted in the past week."

Additionally, it should be able to ingest PDF docs for adhoc uses. 

## DTF - https://github.com/MalasadaTech/defenders-threatmesh-framework

A framework for codifying pivots.

## IOC-comparer - https://github.com/MalasadaTech/ioc-comparer

A tool that performs lookups on indicators (domain indicators for now). It can be used AdHoc, or it could be used in with Thringestor inputs. It compares properties and outputs patterns codified using DTF. 

## hIGMA - https://github.com/MalasadaTech/hIGMA

A sigma inspired data sharing concept. Share pivots just like SIGMA except it specific to pivots and uses DTF. The outputs can feed into masq-monitor, or thrintel sharing. 

## Masq-monitor - https://github.com/MalasadaTech/masq-monitor

A tool that contains pivot queries. It outputs the pivots into easily ingestable formats such as CSV/JSON, for siems, or HTML reports for leadership. 

## Threporter - https://github.com/MalasadaTech/Threporter

A tool to use Thringestor, IOC-comparer, hIGMA, and Masq-monitor as inputs. Threporter should take those inputs and generate a report for the specific activity. 

## STASH - https://github.com/MalasadaTech/STASH

Stores pivots for statistical analysis. Uses input from hIGMA. Output provides gee wiz info for thrintel. 

## Basic Operational Threat Orientation - https://github.com/MalasadaTech/basic-operational-thruntellisearch-orchestrator

A conceptual pipeline that puts all the tools to use. This would automate the processes listed above, and would be the orchestrator that performs the operations by thrintel, thrunt, or thresearch thranalysts. This is "my replacement".



