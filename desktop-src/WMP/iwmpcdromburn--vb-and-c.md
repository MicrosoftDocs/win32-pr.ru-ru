---
title: Интерфейс Ивмпкдромбурн (VB и C) (WMP. h)
description: Предоставляет свойства и методы для управления созданием звуковых компакт-дисков.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- Ивмпкдромбурн (VB и C) интерфейс проигрывателя Windows Media
- Ивмпкдромбурн (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689114"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Интерфейс Ивмпкдромбурн (VB и C#)

Предоставляет свойства и методы для управления созданием звуковых компакт-дисков.

## <a name="members"></a>Элементы

Интерфейс **ивмпкдромбурн (VB и C#)** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **ивмпкдромбурн (VB и C#)** содержит следующие методы.



| Метод                                                                             | Описание                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Удаляет текущий компакт-диск.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Возвращает значение указанного атрибута для компакт-диска.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Предоставляет сведения о дисководе компакт-дисков и носителях.<br/>            |
| [**рефрешстатус**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Обновляет сведения о состоянии текущего записи списка воспроизведения.<br/> |
| [**стартбурн**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Записывает компакт-диск.<br/>                                                 |
| [**стопбурн**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Останавливает процесс записи компакт-дисков.<br/>                                 |



 

### <a name="properties"></a>Свойства

Интерфейс **ивмпкдромбурн (VB и C#)** имеет следующие свойства.



| Свойство                                                                                    | Тип доступа          | Описание                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**бурнформат**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Только для чтения<br/> | Возвращает значение, указывающее тип записываемого компакт-диска.<br/>              |
| [**бурнплайлист**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Только для чтения<br/> | Возвращает текущий список воспроизведения для записи на компакт-диск.<br/>                     |
| [**бурнпрогресс**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Только для чтения<br/> | Возвращает ход выполнения записи компакт-диска в процентах завершения.<br/>                |
| [**бурнстате**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Только для чтения<br/> | Возвращает значение перечисления, указывающее текущее состояние записи.<br/> |
| [**заголовка**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Только для чтения<br/> | Возвращает строку метки тома компакт-диска.<br/>                                 |



 

Получите интерфейс **ивмпкдромбурн** путем приведения интерфейса **ивмпкдром** компакт-диска, который вы хотите записать.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы для Visual Basic .NET и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





