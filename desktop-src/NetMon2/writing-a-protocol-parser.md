---
description: В этом разделе содержатся сведения о написании анализатора протокола, а также примеры функций экспорта, которые должна реализовать библиотека DLL анализатора.
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: Написание средства синтаксического анализа протокола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545002"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="9e1b9-103">Написание средства синтаксического анализа протокола</span><span class="sxs-lookup"><span data-stu-id="9e1b9-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="9e1b9-104">В этом разделе содержатся сведения о написании анализатора протокола, а также примеры функций экспорта, которые должна реализовать библиотека DLL анализатора.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="9e1b9-105">В этот раздел включены следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="9e1b9-106">Термин</span><span class="sxs-lookup"><span data-stu-id="9e1b9-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="9e1b9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9e1b9-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1b9-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Вопросы программирования](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="9e1b9-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="9e1b9-109">Определяет основные советы по программированию, помогающие написать библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="9e1b9-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Реализация функций экспорта средства синтаксического анализа](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="9e1b9-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="9e1b9-111">Содержит примеры реализации функций экспорта.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="9e1b9-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Форматирование отображаемых данных](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="9e1b9-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="9e1b9-113">Определяет процесс форматирования данных, отображаемых в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="9e1b9-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Указание набора следования](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="9e1b9-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="9e1b9-115">Определяет процесс указания набора следования и показывает, как сетевой монитор обращается к следующему набору анализатора для определения следующего протокола.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="9e1b9-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Указание переданного набора](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="9e1b9-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="9e1b9-117">Определяет процесс указания набираемого набора и показывает, как синтаксический анализатор получает доступ к его назначением для получения маркера для следующего протокола.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




