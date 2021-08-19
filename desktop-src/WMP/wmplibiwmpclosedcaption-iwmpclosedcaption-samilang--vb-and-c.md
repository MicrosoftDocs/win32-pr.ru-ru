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
ms.openlocfilehash: 98354d5e1e4f796442dd0347a4ed2796cafdf7297d3829af9b8839d48df00c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930317"
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

## <a name="remarks"></a>Remarks

Файл SAMI может содержать текст для одного или нескольких языков. Языки, доступные для скрытых титров, определяются между тегами <STYLE> и </STYLE> в файле Sami. Идентификатор языка указывается с уникальной буквенно-цифровой строкой, которой предшествует точка (.). Имя, указанное для языка, может быть любой строкой. Например, для определения английского языка (США) можно использовать следующую команду:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Если язык SAMI не указан, по умолчанию используется первый язык, определенный в файле SAMI.

Строка, заданная с помощью **самиланг** , должна соответствовать атрибуту **Name** в описателе языка.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Интерфейс Ивмпклоседкаптион (VB и C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





