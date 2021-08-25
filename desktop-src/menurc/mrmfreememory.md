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
ms.openlocfilehash: 8870281268ff9560d9c82455349f07c3df42e8ab1937b047c4aa9e431b02ed90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825704"
---
# <a name="mrmfreememory-function"></a>Функция Мрмфримемори

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

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

Тип: **Byte \***

Указатель на память, выделенную и возвращаемую [**мрмкреатеконфигинмемори**](mrmcreateconfiginmemory.md), [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md), [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md)или [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

\_ОК, если функция прошла успешно, в противном случае — другое значение. Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только серверные \[ классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мрмсуппорт. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

