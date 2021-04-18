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
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701039"
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
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкоперрор**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

