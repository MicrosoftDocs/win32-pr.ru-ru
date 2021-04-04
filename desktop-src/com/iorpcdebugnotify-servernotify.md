---
title: Иорпкдебугнотифи Сервернотифи, метод
description: Информирует сервер о входящем запросе отладчика от клиента.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- COM-метод Сервернотифи
- Метод Сервернотифи COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Сервернотифи
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6dab7cf68b305e83212045851a88e1cdecdde9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989336"
---
# <a name="iorpcdebugnotifyservernotify-method"></a>Метод Иорпкдебугнотифи:: Сервернотифи

Информирует сервер о входящем запросе отладчика от клиента.

> [!Note]  
> Библиотека импорта, содержащая функцию **сервернотифи** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK). Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Синтаксис


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпорпкдебугалл* 
</dt> <dd>

Указатель на структуру [**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md) , содержащую сведения об уведомлении, которые система com RPC передает отладчику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Н/Д</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Н/Д</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_аргументы инициализации \_ ОРПК**](orpc-init-args.md)
</dt> <dt>

[**дллдебугобжектрпчук**](dlldebugobjectrpchook.md)
</dt> <dt>

[**иорпкдебугнотифи**](iorpcdebugnotify.md)
</dt> </dl>

 

