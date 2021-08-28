---
title: Ивмпклоседкаптион Самиланг, свойство
description: Свойство Самиланг получает или задает язык, отображаемый для скрытых субтитров.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- проигрыватель Windows Media свойства самиланг
- проигрыватель Windows Media свойства самиланг, интерфейс ивмпклоседкаптион
- проигрыватель Windows Media интерфейса ивмпклоседкаптион, свойство самиланг
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9577f7d9030a12a12596fe2cdc2a999922658ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887181"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Свойство Ивмпклоседкаптион:: Самиланг

Свойство **самиланг** получает или задает язык, отображаемый для скрытых субтитров.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является именем, указанным в идентификаторе языка файла Sami.

## <a name="remarks"></a>Комментарии

Файл SAMI может содержать текст для одного или нескольких языков. Языки, доступные для скрытых титров, определяются между &lt; стилями &gt; и </STYLE> ТЕГАМИ в файле Sami. Идентификатор языка указывается с уникальной буквенно-цифровой строкой, которой предшествует точка (.). Имя, указанное для языка, может быть любой строкой. Например, для определения английского языка (США) можно использовать следующую команду:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Если язык SAMI не указан, по умолчанию используется первый язык, определенный в файле SAMI.

Строка, заданная с помощью **самиланг** , должна соответствовать атрибуту **Name** в описателе языка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Интерфейс Ивмпклоседкаптион (VB и C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





