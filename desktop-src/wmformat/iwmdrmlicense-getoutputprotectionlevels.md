---
title: Ивмдрмлиценсе Жетаутпутпротектионлевелс, метод
description: Метод Жетаутпутпротектионлевелс извлекает сведения обо всех уровнях защиты выходных данных (Оплс), назначенных лицензии.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Формат Windows Media, Жетаутпутпротектионлевелс метод
- Жетаутпутпротектионлевелс метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Жетаутпутпротектионлевелс
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771324"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>Метод Ивмдрмлиценсе:: Жетаутпутпротектионлевелс

Метод **жетаутпутпротектионлевелс** извлекает сведения обо всех уровнях защиты выходных данных (оплс), назначенных лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*поплс* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**\_ \_ \_ уровней защиты данных WMDRM**](wmdrm-output-protection-levels.md) , которая получает сведения о ОПЛ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Нет.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмлиценсе**](iwmdrmlicense.md)
</dt> </dl>

 

 





