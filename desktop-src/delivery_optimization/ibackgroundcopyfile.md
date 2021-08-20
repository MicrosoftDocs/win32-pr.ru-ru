---
title: Интерфейс Ибаккграундкопифиле (Deliveryoptimization. h)
description: Ибаккграундкопифиле содержит сведения о файле, который является частью задания. Например, можно использовать методы Ибаккграундкопифиле для получения локальных и удаленных имен файла и сведений о ходе выполнения.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 535002cc6e5763ee7e54d672268f788da6d4456595216722928c37a89c04ccab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101620"
---
# <a name="ibackgroundcopyfile-interface"></a>Интерфейс Ибаккграундкопифиле

**Ибаккграундкопифиле** содержит сведения о файле, который является частью задания. Например, можно использовать методы **ибаккграундкопифиле** для получения локальных и удаленных имен файла и сведений о ходе выполнения.

Чтобы получить указатель интерфейса **ибаккграундкопифиле** , вызовите метод [**Ибаккграундкоперрор::**](ibackgroundcopyerror-getfile-method.md) GetNext или метод [**иенумбаккграундкопифилес:: Next**](ienumbackgroundcopyfiles-next.md) .

## <a name="members"></a>Элементы

Интерфейс **ибаккграундкопифиле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ибаккграундкопифиле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ибаккграундкопифиле** содержит следующие методы.



| Метод                                                            | Описание                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**жетлокалнаме**](ibackgroundcopyfile-getlocalname-method.md)   | Возвращает локальное имя файла.<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | Возвращает ход выполнения перемещения файла.<br/> |
| [**жетремотенаме**](ibackgroundcopyfile-getremotename-method.md) | Извлекает удаленное имя файла.<br/>       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ибаккграундкоперрор**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

