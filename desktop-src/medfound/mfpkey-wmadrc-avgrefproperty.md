---
description: Указывает средний уровень громкости звукового содержимого.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Свойство MFPKEY_WMADRC_AVGREF (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662687"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>МФПКЭЙ \_ вмадрк \_ Авгреф, свойство

Указывает средний уровень громкости звукового содержимого.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмадркаверажереференце

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Комментарии

Это значение можно получить из кодировщика после обработки содержимого. Это значение также может быть задано для декодера в целях динамического управления диапазоном, но оно будет действовать, только если задано свойство [мфпкэй \_ вмадек \_ дркмоде](mfpkey-wmadec-drcmodeproperty.md) .

Дополнительные сведения о динамическом контроле диапазонов см. в статье [функции кодека Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
