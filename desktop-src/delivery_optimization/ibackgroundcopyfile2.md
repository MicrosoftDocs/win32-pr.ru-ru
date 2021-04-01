---
title: Интерфейс IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Используйте интерфейс IBackgroundCopyFile2, чтобы указать новое удаленное имя для файла и получить список загружаемых диапазонов.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Интерфейс IBackgroundCopyFile2
- Интерфейс IBackgroundCopyFile2, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071536"
---
# <a name="ibackgroundcopyfile2-interface"></a>Интерфейс IBackgroundCopyFile2

Используйте интерфейс **IBackgroundCopyFile2** , чтобы указать новое удаленное имя для файла и получить список загружаемых диапазонов.

Интерфейс **IBackgroundCopyFile2** наследуется от интерфейса [**ибаккграундкопифиле**](ibackgroundcopyfile.md) .

Чтобы получить указатель интерфейса **IBackgroundCopyFile2** , вызовите метод **Ибаккграундкопифиле:: QueryInterface** , используя __uuidof (IBackgroundCopyFile2) для идентификатора интерфейса. Используйте указатель интерфейса **IBackgroundCopyFile2** для вызова методов [**ибаккграундкопифиле**](ibackgroundcopyfile.md) и **IBackgroundCopyFile2** .

## <a name="members"></a>Элементы

Интерфейс **IBackgroundCopyFile2** наследует от [**ибаккграундкопифиле**](ibackgroundcopyfile.md). **IBackgroundCopyFile2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IBackgroundCopyFile2** содержит следующие методы.



| Метод                                                             | Описание                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**жетфилеранжес**](ibackgroundcopyfile2-getfileranges-method.md) | Извлекает массив диапазонов, которые необходимо загрузить из URL-адреса.<br/> |
| [**сетремотенаме**](ibackgroundcopyfile2-setremotename-method.md) | Изменяет удаленное имя на новый URL-адрес.<br/>                                 |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 определен как 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопифиле**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





