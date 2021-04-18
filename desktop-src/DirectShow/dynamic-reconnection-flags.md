---
description: Следующие флаги задают уровень динамического повторного подключения, который будет использоваться во время подготовки к просмотру.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Динамические флаги повторного подключения (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675335"
---
# <a name="dynamic-reconnection-flags"></a>Динамические флаги повторного подключения

\[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

Следующие флаги задают уровень динамического повторного подключения, который будет использоваться во время подготовки к просмотру.



| Константа/значение                                                                                                                                                                                                                                            | Описание                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**Коннектф \_ ДИНАМИЧЕСКИЙ \_ нет**</dt> <dt>0x00</dt> </dl>          | Динамическое повторное подключение отсутствует. Загрузите все перед отрисовкой проекта.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**Коннектф \_ ДИНАМИЧЕСКИЕ \_ источники**</dt> <dt>0x01</dt> </dl> | Загружать источники только по мере необходимости.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**Коннектф \_ ДИНАМИЧЕСКИЕ \_ эффекты**</dt> <dt>0x02</dt> </dl> | Зарезервировано. Не используется.<br/>                                                  |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Кедит. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ирендеренгине:: Сетдинамикреконнектлевел**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




