---
description: Тспимессаже — это тип перечисления, определяющий набор дополнительных функций ЛИНИВЕНТ и ФОНИВЕНТ, отображаемых в ТСПИ, которые не отображаются в TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: тспимессаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f74b412d131fc40a13f9da13dc86ba4f31a3becf6bb747e95131bc3bb0e2bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739164"
---
# <a name="tspimessage"></a>тспимессаже

**Тспимессаже** — это тип перечисления, определяющий набор дополнительных функций [**линивент**](/windows/win32/api/tspi/nc-tspi-lineevent) и [**ФОНИВЕНТ**](/windows/desktop/api/tspi/nc-tspi-phoneevent) , отображаемых в ТСПИ, которые не отображаются в TAPI.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_база сообщения \_ тспи
</dt> <dd>

Наименьшее число в диапазоне значений сообщений, относящихся к ТСПИ. Это значение само по себе не имеет смысла, но служит основой для определения других значений.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>Строка \_ невкалл
</dt> <dd>

Указывает, что новый входящий вызов поступил и вводит его в TAPI. Это должно быть первое сообщение, отправленное в TAPI для нового входящего вызова. TAPI возвращает свой непрозрачный идентификатор для вызова в рамках его обработки этого сообщения.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>Строка \_ каллдевспеЦифик
</dt> <dd>

Указывает, что на устройстве вызова произошло событие конкретного устройства.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>Строка \_ каллдевспеЦификфеатуре
</dt> <dd>

Указывает, что на устройстве вызова произошло событие компонента для конкретного устройства.

</dd> </dl>

 

 
