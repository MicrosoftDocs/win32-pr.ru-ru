---
title: Иорпкдебугнотифи Клиентфиллбуффер, метод
description: Отправляет данные из клиентского отладчика в отладчик сервера.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- COM-метод Клиентфиллбуффер
- Метод Клиентфиллбуффер COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Клиентфиллбуффер
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803929"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a>Метод Иорпкдебугнотифи:: Клиентфиллбуффер

Отправляет данные из клиентского отладчика в отладчик сервера.

> [!Note]  
> Библиотека импорта, содержащая функцию **клиентфиллбуффер** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK). Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Синтаксис


```C++
void ClientFillBuffer(
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

[**дллдебугобжектрпчук**](dlldebugobjectrpchook.md)
</dt> <dt>

[**иорпкдебугнотифи**](iorpcdebugnotify.md)
</dt> </dl>

 

