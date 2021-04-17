---
title: IConfigAsfWriter2, метод
description: Метод param извлекает текущее значение указанного параметра конфигурации фильтра.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Метод param Windows Media Format
- Метод param, формат Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 интерфейса Windows Media Format, метод param
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691618"
---
# <a name="iconfigasfwriter2getparam-method"></a>Метод IConfigAsfWriter2:: param

Метод **param** извлекает текущее значение указанного параметра конфигурации фильтра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпарам* \[ окне\]
</dt> <dd>

Указывает параметр для извлечения. Оно должно быть значением, определенным в перечислении [ \_ \_ \_ param асфвритерконфиг](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*pdwParam1* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает значение параметра, указанного в *двпарам*.

</dd> <dt>

*pdwParam2* \[ заполняет\]
</dt> <dd>

Не используется, должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: Сетпарам**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 