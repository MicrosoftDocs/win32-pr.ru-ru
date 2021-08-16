---
title: Идвритефонтфаллбаккбуилдер Аддмаппинг, метод
description: Добавляет одно сопоставление в список. Вызывайте его один раз для каждого дополнительного сопоставления.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Непосредственная запись метода Аддмаппинг
- Прямая запись метода Аддмаппинг, интерфейс Идвритефонтфаллбаккбуилдер
- Прямая запись интерфейса Идвритефонтфаллбаккбуилдер, метод Аддмаппинг
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6496ac9ef9bdfa574cc2c4710ed4620fd855dbf5eff2b22885b32bf343d141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650444"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Метод Идвритефонтфаллбаккбуилдер:: Аддмаппинг

Добавляет одно сопоставление в список. Вызывайте его один раз для каждого дополнительного сопоставления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*остаются* 
</dt> <dd>

Тип: **[ **дврите \_ \_ диапазон Юникода**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

Диапазоны Юникода, которые применяются к этому сопоставлению.

</dd> <dt>

*ранжескаунт* 
</dt> <dd>

Тип: **UINT32**

Число диапазонов Юникода.

</dd> <dt>

*таржетфамилинамес* \[ окне\]
</dt> <dd>

Тип: **const WCHAR \* \***

Список строк имен целевых семейств.

</dd> <dt>

*таржетфамилинамескаунт* 
</dt> <dd>

Тип: **UINT32**

Число имен целевых семейств.

</dd> <dt>

*фонтколлектион* \[ в необязательное\]
</dt> <dd>

Тип: **[ **идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Необязательная коллекция явных шрифтов для этого сопоставления.

</dd> <dt>

*localeName* \[ в необязательное\]
</dt> <dd>

Тип: **const WCHAR \***

Языковой стандарт контекста.

</dd> <dt>

*басефамилинаме* \[ в необязательное\]
</dt> <dd>

Тип: **const WCHAR \***

Имя базового семейства для сопоставления, если применимо.

</dd> <dt>

*масштаб* 
</dt> <dd>

Тип: **float**

Коэффициент масштабирования для умножения целевого шрифта результата на.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идвритефонтфаллбаккбуилдер**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

