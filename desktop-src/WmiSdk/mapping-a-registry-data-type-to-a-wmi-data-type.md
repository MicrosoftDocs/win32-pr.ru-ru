---
description: Приложение должно создать свойства с типом данных, который сопоставляется с типом данных реестра.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Сопоставление типа данных реестра с типом данных WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b96a3bcda0060e376427375059f006e3241118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546375"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Сопоставление типа данных реестра с типом данных WMI

Приложение должно создать свойства с типом данных, который сопоставляется с типом данных реестра. Не нужно указывать тип данных реестра в методах, которые создают, получают или устанавливают значения реестра. Однако входной параметр, содержащий значение, должен иметь правильный тип данных WMI. Например, если приложение получает данные **reg \_ DWORD** из реестра, то класс, который получает данные, должен включать свойство **UInt32** .

В следующей таблице перечислены сопоставления между реестром и типами данных WMI, используемыми в методах [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) .



| Тип данных реестра      | Тип данных WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_двоичный файл REG**         | Массив **Uint8**<br/> Массив значений, не превышающий 255 или шестнадцатеричное FF. Например, следующий Visual Basic код скрипта создает массив, соответствующий этому типу данных.<br/> `BinArray = Array(&H01, &Ha2)`<br/> Методу класса [**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) [**сетбинаривалуе**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) требуется **\_ двоичный** тип данных reg.<br/>                                                                                          |
| **REG \_ DWORD**          | **UInt32**, **Sint32** или Visual Basic **целое число**<br/> Одно 32-разрядное значение. Для методов класса [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) , [**жетдвордвалуе**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) и [**Сетдвордвалуе**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) , требуется тип данных **reg \_ DWORD** .<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **string**<br/> Методу класса [**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) требуется тип данных **reg \_ SZ** .<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **UInt64**.<br/> Одно 64-разрядное значение. Для методов класса [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) , [**жетквордвалуе**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) и [**Сетквордвалуе**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) , требуется тип данных **reg \_ QWORD** .<br/>                                                                                                                                                                                                         |
| **\_распаковать \_ SZ**     | **string**<br/> Развернутые строки — это специальные строки, представляющие системные переменные среды. Например, следующий код VBScript создает строку, представляющую переменную **локальной среды \_ \_ пользователя hKey** Temp.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> Методу класса [**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) [**сетекспандедстрингвалуе**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) требуется тип данных **\_ expand \_ SZ** .<br/> |
| **REG \_ Multi \_ SZ**      | Массив **строк**<br/> Многострочный тип данных содержит несколько строк. Например, следующий код VBScript создает массив, соответствующий этому типу данных.<br/> `MultiValue = Array("first", "second", "third")`<br/> Методу класса [**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) [**сетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) требуется тип данных **reg \_ Multi \_ SZ** .<br/>                                                                     |
| **\_список ресурсов \_ реестра** | По мере необходимости. Дополнительные сведения см. в разделе [Описание ресурса для реестра](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Определение классов для поставщика системного реестра](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

