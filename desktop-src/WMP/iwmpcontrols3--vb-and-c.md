---
title: Интерфейс IWMPControls3 (VB и C) (WMP. h)
description: Предоставляет свойства и методы для выбора и поддержки звукового языка, дополняют интерфейс IWMPControls2. В дополнение к свойствам и методам, унаследованным от IWMPControls2, интерфейс IWMPControls3 предоставляет следующие свойства.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- IWMPControls3 (VB и C) интерфейс проигрывателя Windows Media
- IWMPControls3 (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9788dbd1b5910d655cbaa17055c76a0ae6d0280e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689111"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>Интерфейс IWMPControls3 (VB и C#)

Предоставляет свойства и методы для выбора и поддержки звукового языка, дополняют интерфейс **IWMPControls2** .

В дополнение к свойствам и методам, унаследованным от **IWMPControls2**, интерфейс **IWMPControls3** предоставляет следующие свойства.

## <a name="members"></a>Элементы

Интерфейс **IWMPControls3 (VB и C#)** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **IWMPControls3 (VB и C#)** содержит следующие методы.



| Метод                                                                                                         | Описание                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**жетаудиолангуажедескриптион**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Возвращает описание для аудио-языка, соответствующего указанному индексу, основанному на единице.<br/> |
| [**жетаудиолангуажеид**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Возвращает код языка для указанного индекса языкового звука.<br/>                                         |
| [**жетлангуаженаме**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Возвращает имя аудио языка с указанным LCID.<br/>                                |



 

### <a name="properties"></a>Свойства

Интерфейс **IWMPControls3 (VB и C#)** имеет следующие свойства.



| Свойство                                                                                                              | Тип доступа           | Описание                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аудиолангуажекаунт**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Только для чтения<br/>  | Возвращает число поддерживаемых аудио языков. <br/>                                                                                            |
| [**куррентаудиолангуаже**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Чтение/запись<br/> | Возвращает или задает код локали (LCID) звукового языка для воспроизведения. <br/>                                                           |
| [**куррентаудиолангуажеиндекс**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Чтение/запись<br/> | Возвращает или задает отсчитываемый от единицы индекс, соответствующий звуковому языку для воспроизведения. <br/>                                                   |
| [**куррентпоситионтимекоде**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Чтение/запись<br/> | Возвращает или задает текущую позицию в текущем элементе мультимедиа, используя формат кода времени. Сейчас это свойство поддерживает код времени SMPTE. <br/> |



 

Получите интерфейс **IWMPControls3** путем приведения значения, возвращаемого свойством [**аксвиндовсмедиаплайер. ктлконтролс**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы для Visual Basic .NET и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPControls2 (VB и C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





