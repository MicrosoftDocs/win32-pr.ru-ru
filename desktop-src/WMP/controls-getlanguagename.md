---
title: Controls. Жетлангуаженаме, метод
description: Метод Жетлангуаженаме извлекает имя звукового языка с указанным кодом локали (LCID).
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Жетлангуаженаме метод Windows Media Player
- метод Жетлангуаженаме Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Жетлангуаженаме
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698901"
---
# <a name="controlsgetlanguagename-method"></a>Controls. Жетлангуаженаме, метод

Метод **жетлангуаженаме** извлекает имя звукового языка с указанным кодом локали (LCID).

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Код языка* \[ в\]
</dt> <dd>

**Число** (**длинное**), определяющее код языка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Комментарии

Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Controls. Аудиолангуажекаунт**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. Куррентаудиолангуаже**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. Куррентаудиолангуажеиндекс**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. Жетаудиолангуажедескриптион**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. Жетаудиолангуажеид**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





