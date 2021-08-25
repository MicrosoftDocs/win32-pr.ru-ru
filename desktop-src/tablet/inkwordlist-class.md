---
description: Представляет список слов, которые можно использовать для улучшения результатов распознавания.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Класс Инквордлист (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: fe46cf8f1befaf2717cfcf0a8e131113ed4552843bd3b6572364c27f3418ab34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938674"
---
# <a name="inkwordlist-class"></a>Класс Инквордлист

Представляет список слов, которые можно использовать для улучшения результатов распознавания.

**Инквордлист** имеет следующие типы членов:

-   [Интерфейсы](#interfaces)
-   [Методы](#methods)

### <a name="interfaces"></a>Интерфейсы

Класс **инквордлист** определяет эти интерфейсы.



| Интерфейс        | Описание                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **иинквордлист** | Этот объект реализует COM-интерфейс **иинквордлист** .<br/> |



 

### <a name="methods"></a>Методы

Класс **инквордлист** содержит следующие методы.



| Метод                                       | Описание                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**аддворд**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Добавляет одно слово в **инквордлист**.<br/>                   |
| [**AutoMerge**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Выполняет слияние другого **инквордлист** с этим **инквордлист**.<br/> |
| [**ремовеворд**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Удаляет одно слово из **инквордлист**.<br/>                |



 

## <a name="remarks"></a>Remarks

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Константы фактоид](factoid-constants.md)
</dt> <dt>

[**Класс Инкрекогнизерконтекст**](inkrecognizercontext-class.md)
</dt> </dl>

 

