---
description: Перечисляет имена доступных поставщиков служб шифрования (CSP).
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Метод Искрденр:: Енумкспнаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546682"
---
# <a name="iscrdenrenumcspname-method"></a>Метод Искрденр:: Енумкспнаме

Метод **енумкспнаме** перечисляет имена доступных [*поставщиков служб шифрования*](../secgloss/c-gly.md) (CSP).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс последовательности перечисления.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Зарезервировано для последующего использования. Присвойте этому параметру значение 0.

</dd> <dt>

*пбстркспнаме* \[ заполняет\]
</dt> <dd>

Указатель на строку, которая возвращает имя перечисленного CSP.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Строка, представляющая имя перечисленного CSP.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искрденр**](iscrdenr.md)
</dt> <dt>

[**Искрденр:: Кспкаунт**](iscrdenr-cspcount.md)
</dt> <dt>

[**Искрденр:: CSPName**](iscrdenr-cspname.md)
</dt> </dl>

 

 
