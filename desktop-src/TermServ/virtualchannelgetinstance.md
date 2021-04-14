---
title: Точка входа Виртуалчаннелжетинстанце
description: Вызывается для того, чтобы подключаемый модуль создает экземпляр интерфейса Ивтсплугин для всех подключаемых модулей, реализованных библиотекой DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов точки входа Виртуалчаннелжетинстанце
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415145"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Точка входа Виртуалчаннелжетинстанце

Вызывается для того, чтобы подключаемый модуль создает экземпляр интерфейса [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) для всех подключаемых модулей, РЕАЛИЗОВАНных библиотекой DLL.

> [!Note]
>
> Эта функция реализуется подключаемым модулем и должна быть экспортирована по имени таким, что приложение может использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к функции.
>
> Прототип для этой функции не содержится в файле общедоступного заголовка, поэтому его необходимо объявить в точности так, как показано.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*рефиид* \[ окне\]
</dt> <dd>

Указывает тип возвращаемого интерфейса. Это должен быть **IID \_ ивтсплугин**.

</dd> <dt>

*пнумобжс* \[ в, out\]
</dt> <dd>

Адрес переменной **ulong** , которая получает число извлеченных интерфейсов.

</dd> <dt>

*ппобжаррай* \[ заполняет\]
</dt> <dd>

Адрес массива указателей, получающих указатели интерфейса. Если этот параметр имеет **значение NULL**, реализация должна поставить число подключаемых модулей, реализованных библиотекой DLL, в параметре *пнумобжс* . Это позволяет вызывающему объекту выделить правильный массив размера для *ппобжаррай*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если точка входа прошла успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



 

