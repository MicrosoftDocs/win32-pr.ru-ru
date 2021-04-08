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
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791221"
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

## <a name="remarks"></a>Комментарии

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) с помощью метода [**Add \_ коннектионстатусчанжед**](ibasicdevice-add-connectionstatuschanged.md) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ коннектионстатусчанжед**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 