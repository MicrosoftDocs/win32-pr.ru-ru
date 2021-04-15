---
title: Иконфигасфвритер Жетиндексмоде, метод
description: Метод Жетиндексмоде извлекает текущий режим временного индекса.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Формат Windows Media, Жетиндексмоде метод
- Жетиндексмоде метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жетиндексмоде
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413217"
---
# <a name="iconfigasfwritergetindexmode-method"></a>Метод Иконфигасфвритер:: Жетиндексмоде

Метод **жетиндексмоде** извлекает текущий режим временного индекса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбиндексфиле* \[ заполняет\]
</dt> <dd>

Указатель на переменную типа **bool** , которая получает параметр режима временных индексов. Значение **true** указывает, что модуль записи WM ASF настроен для записи временных индексированных файлов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы определить, настроен ли [модуль записи WM ASF](wm-asf-writer-filter.md) для записи файлов ASF с временным индексированием. Дополнительные сведения о временных индексированных и индексированных файлах см. в разделе Примечания для [**иконфигасфвритер:: сетиндексмоде**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 