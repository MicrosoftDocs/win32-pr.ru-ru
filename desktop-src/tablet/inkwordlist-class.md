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
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703053"
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



 

## <a name="remarks"></a>Комментарии

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Константы фактоид](factoid-constants.md)
</dt> <dt>

[**Класс Инкрекогнизерконтекст**](inkrecognizercontext-class.md)
</dt> </dl>

 

