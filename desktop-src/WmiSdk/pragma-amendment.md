---
description: Направляет компилятор MOF для разделения MOF-файла на зависящие от языка и языковые версии.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: поправка директивы pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6204ac7f3cd78de8d2eed9740fc165475d387e65284bcbf6be1ea10ed91a0926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992734"
---
# <a name="pragma-amendment"></a>поправка директивы pragma

Команда препроцессора " **директива pragma** Reprocess" направляет компилятор MOF для разделения MOF-файла на зависящие от языка и языковые версии. MOF-файл, зависящий от языка, перемещает измененные квалификаторы в пространство имен для определенного языкового стандарта. Затем вы компилируете файлы MOF, не зависящие от языка и на языке, для хранения сведений о классах в репозитории WMI.

## <a name="examples"></a>Примеры

В следующем примере показано, как создать MOF-файл, содержащий измененные квалификаторы. Затем MOF-код можно скомпилировать с помощью следующей команды:

**mofcomp** **-MOF: лнмоф. mof** **-МФЛ: лсмоф. МФЛ** **мастермоф. mof**

Эта команда предписывает компилятору MOF создать два MOF-файла из исходного Мастермоф. mof. Компилятор MOF создает не зависящую от языка версию MOF-файла с именем Лнмоф. mof, при этом удаляются все зависящие от языка элементы. Компилятор также создает второй, зависящий от языка MOF-файл с именем Лсмоф. МФЛ, который содержит только те элементы, которые необходимо локализовать.

> [!Note]  
> При разделении MOF-файла **с квалификатором или с помощью** **директивы pragma** reby необходимо указать параметры **-MOF** и **-МФЛ** . В противном случае компилятор не создает никаких выходных файлов. Затем необходимо скомпилировать два выходных файла, чтобы сделать сведения о классе доступными для инструментария WMI.

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Команды препроцессора](preprocessor-commands.md)
</dt> </dl>

 

 




