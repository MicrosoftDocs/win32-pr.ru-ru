---
title: External. Савекуррентвиевтолибрари, метод
description: Метод Савекуррентвиевтолибрари создает список воспроизведения из элементов мультимедиа в текущем представлении и сохраняет список воспроизведения в локальной библиотеке.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- Савекуррентвиевтолибрари метод Windows Media Player
- Савекуррентвиевтолибрари метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Савекуррентвиевтолибрари
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694485"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>External. Савекуррентвиевтолибрари, метод

Метод **савекуррентвиевтолибрари** создает список воспроизведения из элементов мультимедиа в текущем представлении и сохраняет список воспроизведения в локальной библиотеке.

## <a name="syntax"></a>Синтаксис


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фриендлилистнаме* \[ окне\]
</dt> <dd>

**Строка** , указывающая понятное имя для списка воспроизведения. Проигрыватель Windows Media отображает это имя в пользовательском интерфейсе.

</dd> <dt>

*Локальный* \[ окне\]
</dt> <dd>

**Логическое значение** , указывающее, является ли список воспроизведения динамическим или статическим. **Значение true** указывает Dynamic, а **false** — статический.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





