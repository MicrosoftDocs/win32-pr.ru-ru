---
description: Представляет метод, который вызывается при завершении асинхронного действия.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Интерфейс Асинкактионкомплетедхандлер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711063"
---
# <a name="asyncactioncompletedhandler-interface"></a>Интерфейс Асинкактионкомплетедхандлер

Представляет метод, который вызывается при завершении асинхронного действия.

## <a name="members"></a>Элементы

Интерфейс **асинкактионкомплетедхандлер** наследует от [**иасинЦинфо**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **Асинкактионкомплетедхандлер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **асинкактионкомплетедхандлер** содержит следующие методы.



| Метод                                               | Описание                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Вызвать**](asyncactioncompletedhandler-invoke.md) | Вызывает метод, вызываемый при завершении указанного асинхронного действия.<br/> |



 

## <a name="remarks"></a>Комментарии

Назначьте **Асинкактионкомплетедхандлер** [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) , чтобы получить уведомление о завершении асинхронного действия.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иасинЦинфо**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

