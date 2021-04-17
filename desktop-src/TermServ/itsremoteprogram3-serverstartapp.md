---
title: ITSRemoteProgram3 Серверстартапп, метод
description: Указывает приложение, запускаемое в удаленном сеансе.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Серверстартапп
- Службы удаленных рабочих столов метода Серверстартапп, интерфейс ITSRemoteProgram3
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram3, метод Серверстартапп
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682077"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>Метод ITSRemoteProgram3:: Серверстартапп

Указывает приложение, запускаемое в удаленном сеансе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраппусермоделид* \[ окне\]
</dt> <dd></dd> <dt>

*бстраргументс* \[ окне\]
</dt> <dd></dd> <dt>

*вбекспанденвваринаргументсонсервер* \[ окне\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





