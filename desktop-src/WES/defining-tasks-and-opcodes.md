---
title: Определение задач и кодов операций
description: Поставщики используют задачи и коды операций для логической группировки событий. Группирование событий помогает клиентам запрашивать только те события, которые содержат определенные сочетания задач и операций.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533074"
---
# <a name="defining-tasks-and-opcodes"></a>Определение задач и кодов операций

Поставщики используют задачи и коды операций для логической группировки событий. Группирование событий помогает клиентам запрашивать только те события, которые содержат определенные сочетания задач и операций. Как правило, задачи используются для задания основного компонента поставщика, такого как компонент сети или компонента базы данных. Затем можно использовать коды операций для обнаружения операций, выполняемых компонентом, таких как операции отправки и получения сетевого компонента. Если у вас только один компонент, можно использовать задачу для отражения основной операции в компоненте, например соединения или отключения, и использовать код операции для отражения действия в рамках операции, например чтения реестра. Кроме того, код операции можно использовать без указания задачи. Использование задач и кодов операций для группировки событий потребителю полностью завершено.

Чтобы определить задачу, используйте элемент **Task** . Чтобы определить код операции, используйте элемент **opcode** . Можно указать до 228 кодов операций. **Значение** задачи должно быть больше 0. Коды операций должны быть в диапазоне от 11 до 239. Файл Winmeta.xml определяет общие операции, которые можно использовать вместо определения собственного.

В следующем примере показано, как определить несколько задач и кодов операций.

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
