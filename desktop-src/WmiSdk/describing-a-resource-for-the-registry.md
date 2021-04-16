---
description: Системный реестр содержит данные, связанные с ресурсами.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Описание ресурса для реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702719"
---
# <a name="describing-a-resource-for-the-registry"></a>Описание ресурса для реестра

Системный реестр содержит данные, связанные с ресурсами. Эти данные находятся в следующем разделе реестра и хранятся в специальном типе данных реестра с именем **reg \_ Resource \_ List**. Приложения могут получать связанные с ресурсами данные через поставщик системного реестра. В реестр можно добавлять и изменять системные ресурсы.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

В следующей процедуре описывается хранение сведений о ресурсах в системном реестре.

**Сохранение сведений, связанных с ресурсами, в системном реестре**

1.  Создайте строку, содержащую следующие поля.

    

    <table>
    <thead>
    <tr class="header">
    <th>Поле</th>
    <th>Содержит</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Тип интерфейса</td>
    <td>Одно из следующих значений:<br/> <dl> Внутренние<br />
    Диспетчера<br />
    Использует<br />
    Микроканал<br />
    турбочаннел<br />
    пЦибус<br />
    вмебус<br />
    нубус<br />
    пкмЦиабус<br />
    кбус<br />
    мпибус<br />
    мпсабус<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Номер шины</td>
    <td>Целое число, указывающее номер шины.</td>
    </tr>
    <tr class="odd">
    <td>Частичный номер дескриптора</td>
    <td>Целое число, указывающее номер дескриптора.</td>
    </tr>
    <tr class="even">
    <td>Тип смещения или объединения</td>
    <td>Одно из следующих значений:<br/> <dl> Порт. Запуск<br />
    Порт. PhysicalAddress<br />
    Порт. Длина<br />
    Прервать. уровень<br />
    Interrupt. Vector<br />
    Прерывание. сходство<br />
    Память. Запуск<br />
    Memory. PhysicalAddress<br />
    Память. Длина<br />
    Канал DMA.<br />
    DMA. Port<br />
    DMA. Reserved1<br />
    ДевицеспеЦификдата. DataSize<br />
    ДевицеспеЦификдата. Reserved1<br />
    ДевицеспеЦификдата. Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Поместите строку в соответствующий раздел раздела реестра.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

В следующем примере кода описывается допустимый дескриптор ресурса.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

В следующем примере кода показан допустимый синтаксис MOF для получения дескриптора ресурса.

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




