---
title: Событие Коннектионстатусчанжед
description: Происходит при изменении состояния сетевого подключения устройства.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API потоковой передачи мультимедиа для события Коннектионстатусчанжед
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060434"
---
# <a name="connectionstatuschanged-event"></a>Событие Коннектионстатусчанжед

Происходит при изменении состояния сетевого подключения устройства.

## <a name="syntax"></a>Синтаксис


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) с помощью метода [**Add \_ коннектионстатусчанжед**](ibasicdevice-add-connectionstatuschanged.md) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ коннектионстатусчанжед**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 