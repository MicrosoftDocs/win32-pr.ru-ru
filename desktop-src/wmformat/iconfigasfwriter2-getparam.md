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
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809144"
---
# <a name="iconfigasfwriter2getparam-method"></a>Метод IConfigAsfWriter2:: param

Метод **param** извлекает текущее значение указанного параметра конфигурации фильтра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
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

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: Сетпарам**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 