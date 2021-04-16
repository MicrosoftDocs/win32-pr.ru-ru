---
title: Функция Мрмфримемори (Мрмресаурцеиндексер. h)
description: Освобождает память, выделенную Мрмкреатеконфигинмемори, Мрмкреатересаурцефилеинмемори, Мрмдумпприфилеинмемори и Мрмдумппридатаинмемори.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Меню функций Мрмфримемори и другие ресурсы
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661959"
---
# <a name="mrmfreememory-function"></a>Функция Мрмфримемори

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Освобождает память, выделенную [**мрмкреатеконфигинмемори**](mrmcreateconfiginmemory.md), [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md), [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md)и [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md). Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*данные* \[ окне\]
</dt> <dd>

Тип: **Byte \** _

Указатель на память, выделенную и возвращаемую [_ *мрмкреатеконфигинмемори* *](mrmcreateconfiginmemory.md), [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md), [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md)или [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

\_ОК, если функция прошла успешно, в противном случае — другое значение. Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только классические приложения Windows Server\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мрмсуппорт. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

