---
description: устанавливает указанный объект ActiveX.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Метод Иеаксисистеминсталлер:: Инитиализесистеминсталлер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9619557395ede0510e04378a03f2ded32fa7a9c829c8c6f40acdaf58b8e0fda2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414654"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>Метод Иеаксисистеминсталлер:: Инитиализесистеминсталлер

метод **инитиализесистеминсталлер** устанавливает указанный объект ActiveX.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бструрл* \[ окне\]
</dt> <dd>

URL-адрес устанавливаемого объекта ActiveX.

</dd> <dt>

*двклиентпид* \[ окне\]
</dt> <dd>

Идентификатор процесса вызывающего процесса.

</dd> <dt>

*пкаллбакк* \[ окне\]
</dt> <dd>

указатель на экземпляр интерфейса [**иеаксисервицекаллбакк**](ieaxiservicecallback.md) , который проверяет, разрешена ли установка объекта ActiveX.

</dd> <dt>

*пбстрнонце* \[ заполняет\]
</dt> <dd>

контекст, который можно использовать для совместного использования сведений о состоянии в вызовах других методов, используемых для проверки и загрузки объекта ActiveX.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista Business, Windows vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисистеминсталлер определен как a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иеаксисистеминсталлер**](ieaxisysteminstaller.md)
</dt> </dl>

 

