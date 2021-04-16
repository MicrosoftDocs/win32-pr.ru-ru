---
description: '\_Константы линелокатионоптион определяют значения, используемые в элементе двоптионс структуры линелокатионентри, возвращаемой как часть структуры линетранслатекапс, возвращаемой линежеттранслатекапс.'
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Константы LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679587"
---
# <a name="linelocationoption_-constants"></a>\_Константы линелокатионоптион

Константы **\_ линелокатионоптион** определяют значения, используемые в элементе **двоптионс** структуры [**линелокатионентри**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) , возвращаемой как часть структуры [**линетранслатекапс**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) , возвращаемой [**линежеттранслатекапс**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**ЛИНЕЛОКАТИОНОПТИОН \_ пулседиал**
</dt> <dd> <dl> <dt>



По умолчанию в этом расположении используется импульсный набор номеров. Если этот бит задан, [**линетранслатеаддресс**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) вставит в начало строки с набором номера "P" модификатор набора, возвращаемый при выборе этого расположения. Если этот бит не задан, **линетранслатеаддресс** вставит в начало строки "T" модификатор вызова.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Не расширяемый. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




