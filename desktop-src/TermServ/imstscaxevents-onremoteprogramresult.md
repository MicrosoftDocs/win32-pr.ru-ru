---
title: Имстскаксевентс Онремотепрограмресулт, метод
description: Вызывается, когда программа RemoteApp возвращает результат в клиентский элемент управления.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотепрограмресулт
- Службы удаленных рабочих столов метода Онремотепрограмресулт, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотепрограмресулт
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807fbd49cc6222925f34a7e7c007fef54cbc9a3db2566f024ebc0188e9c95113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129666"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a>Метод Имстскаксевентс:: Онремотепрограмресулт

Вызывается, когда программа RemoteApp возвращает результат в клиентский элемент управления.

## <a name="syntax"></a>Синтаксис


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрремотепрограм* \[ окне\]
</dt> <dd>

Имя программы RemoteApp.

</dd> <dt>

*леррор* \[ окне\]
</dt> <dd>

Результат попытки запуска программы RemoteApp.

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**ремотеаппресулток** (0 (0x0))


</dt> <dd>

Программа RemoteApp успешно запущена.

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**ремотеаппресултлоккед** (1 (0x1))


</dt> <dd>

Удаленный сеанс заблокирован, и программа RemoteApp не может быть запущена. Пользователь должен ввести свои учетные данные, чтобы разблокировать сеанс, а затем запустить программу RemoteApp.

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**ремотеаппресултпротоколеррор** (2 (0x2))


</dt> <dd>

Программа RemoteApp вернула ошибку протокола.

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**ремотеаппресултнотинвхителист** (3 (0x3))


</dt> <dd>

Программа RemoteApp не находится в списке утвержденных серверов узла сеансов удаленных рабочих столов.

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**ремотеаппресултнетворкпасдениед** (4 (0x4))


</dt> <dd>

Сетевой путь к удаленному приложению RemoteApp был отклонен.

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**ремотеаппресултфиленотфаунд** (5 (0x5))


</dt> <dd>

Файл программы RemoteApp не найден.

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**ремотеаппресултфаилуре** (6 (0x6))


</dt> <dd>

Не удалось запустить программу RemoteApp.

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**ремотеаппресулсукнотлоадед** (7 (0x7))


</dt> <dd>

Невозможно запустить программу RemoteApp, так как в настоящий момент в сеансе отображается защищенный рабочий стол.

</dd> </dl> </dd> <dt>

*вбисексекутабле* \[ окне\]
</dt> <dd>

Указывает, было ли удаленное приложение RemoteApp запущено напрямую с помощью имени исполняемого файла или косвенно с помощью сопоставления файлов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что программа RemoteApp вернула результат.

этот метод вызывается сразу после того, как элемент управления ActiveX пытается запустить программу RemoteApp, а параметр *леррор* указывает результат попытки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





