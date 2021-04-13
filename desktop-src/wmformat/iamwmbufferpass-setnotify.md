---
title: Иамвмбуфферпасс Сетнотифи, метод
description: Метод Сетнотифи используется приложениями для предоставления модулю записи WM ASF или фильтра чтения WM ASF указателя на интерфейс Иамвмбуфферпасскаллбакк приложения.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Формат Windows Media, Сетнотифи метод
- Сетнотифи метод Windows Media Format, интерфейс Иамвмбуфферпасс
- Интерфейс Иамвмбуфферпасс Windows Media Format, метод Сетнотифи
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413495"
---
# <a name="iamwmbufferpasssetnotify-method"></a>Метод Иамвмбуфферпасс:: Сетнотифи

Метод **сетнотифи** используется приложениями для предоставления модулю записи WM ASF или фильтра [чтения WM ASF](wm-asf-reader-filter.md) указателя на интерфейс [**иамвмбуфферпасскаллбакк**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкаллбакк* \[ окне\]
</dt> <dd>

Указатель на интерфейс **иамвмбуфферпасскаллбакк** приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Вызовите этот метод перед переводом графа фильтра в состояние выполнения.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамвмбуфферпасс**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 