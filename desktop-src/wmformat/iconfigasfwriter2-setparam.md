---
title: IConfigAsfWriter2 Сетпарам, метод
description: Метод Сетпарам задает значение указанного параметра конфигурации фильтра.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Формат Windows Media, Сетпарам метод
- Сетпарам метод Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 Windows Media Format, метод Сетпарам
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691598"
---
# <a name="iconfigasfwriter2setparam-method"></a>Метод IConfigAsfWriter2:: Сетпарам

Метод **сетпарам** задает значение указанного параметра конфигурации фильтра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпарам* \[ окне\]
</dt> <dd>

Задает заданный параметр. Оно должно быть значением, определенным в перечислении [ \_ \_ \_ param асфвритерконфиг](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*dwParam1* \[ окне\]
</dt> <dd>

Указывает значение, присваиваемое параметру *двпарам* .

</dd> <dt>

*dwParam2* \[ окне\]
</dt> <dd>

Не используется; значение должно быть равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: param**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 