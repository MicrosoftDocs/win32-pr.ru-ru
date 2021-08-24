---
title: Интерфейс Иенумбаккграундкопифилес (Deliveryoptimization. h)
description: Используйте интерфейс Иенумбаккграундкопифилес для перечисления файлов, содержащихся в задании. Чтобы получить указатель интерфейса Иенумбаккграундкопифилес, вызовите метод использованием метода ibackgroundcopyjob Енумфилес.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, описание
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c6cf97975d583a99145e32482bc097ebd6ce3cc052e62560a34f7f78c1f88ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635684"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Интерфейс Иенумбаккграундкопифилес

Используйте интерфейс **иенумбаккграундкопифилес** для перечисления файлов, содержащихся в задании. Чтобы получить указатель интерфейса **иенумбаккграундкопифилес** , вызовите метод [**использованием метода ibackgroundcopyjob:: енумфилес**](ibackgroundcopyjob-enumfiles.md) .

## <a name="members"></a>Элементы

Интерфейс **иенумбаккграундкопифилес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иенумбаккграундкопифилес** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иенумбаккграундкопифилес** содержит следующие методы.



| Метод                                                | Описание                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Извлекает количество элементов в перечислении.<br/>                  |
| [**Далее**](ienumbackgroundcopyfiles-next.md)         | Возвращает заданное число элементов последовательности перечисления.<br/> |
| [**Перезапуск**](ienumbackgroundcopyfiles-reset.md)       | Сбрасывает последовательность перечисления в начало.<br/>                  |
| [**Сразу**](ienumbackgroundcopyfiles-skip.md)         | Пропускает заданное число элементов в последовательности перечисления.<br/>     |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: Енумфилес**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

