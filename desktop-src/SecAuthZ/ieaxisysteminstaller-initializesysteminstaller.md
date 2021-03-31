---
description: Устанавливает указанный объект ActiveX.
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
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912431"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>Метод Иеаксисистеминсталлер:: Инитиализесистеминсталлер

Метод **инитиализесистеминсталлер** устанавливает указанный объект ActiveX.

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

Указатель на экземпляр интерфейса [**иеаксисервицекаллбакк**](ieaxiservicecallback.md) , который проверяет, разрешена ли установка объекта ActiveX.

</dd> <dt>

*пбстрнонце* \[ заполняет\]
</dt> <dd>

Контекст, который можно использовать для совместного использования сведений о состоянии в вызовах других методов, используемых для проверки и загрузки объекта ActiveX.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисистеминсталлер определен как a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иеаксисистеминсталлер**](ieaxisysteminstaller.md)
</dt> </dl>

 

