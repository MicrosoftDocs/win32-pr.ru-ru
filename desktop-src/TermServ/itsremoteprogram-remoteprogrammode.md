---
title: Итсремотепрограм Ремотепрограммоде, свойство
description: режим Windows Server 2008 R2 RemoteApp.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Ремотепрограммоде
- Службы удаленных рабочих столов свойства Ремотепрограммоде, интерфейс Итсремотепрограм
- Службы удаленных рабочих столов интерфейса Итсремотепрограм, свойство Ремотепрограммоде
- Службы удаленных рабочих столов свойства Ремотепрограммоде, интерфейс ITSRemoteProgram2
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram2, свойство Ремотепрограммоде
- Службы удаленных рабочих столов свойства Ремотепрограммоде, интерфейс ITSRemoteProgram3
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram3, свойство Ремотепрограммоде
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36f450e6cbfec3922a56a42bc2f1f61466774eeff46c0987b6fad4ca9dc9731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124824"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>Свойство Итсремотепрограм:: Ремотепрограммоде

режим Windows Server 2008 R2 RemoteApp.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>Значение свойства

Режим RemoteApp. Если задано **значение \_ true**, режим RemoteApp включен, а удаленный сеанс будет размещать программы RemoteApp. Если задано значение " **Variant \_ false** " (по умолчанию), режим RemoteApp не включен. В удаленном сеансе будет размещен удаленный рабочий стол.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ итсремотепрограм определен как FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**итсремотепрограм**](itsremoteprogram.md)
</dt> </dl>

 

 





