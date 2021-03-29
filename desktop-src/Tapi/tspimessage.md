---
description: Тспимессаже — это тип перечисления, определяющий набор дополнительных функций ЛИНИВЕНТ и ФОНИВЕНТ, отображаемых в ТСПИ, которые не отображаются в TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: тспимессаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811440"
---
# <a name="tspimessage"></a><span data-ttu-id="ebaf6-103">тспимессаже</span><span class="sxs-lookup"><span data-stu-id="ebaf6-103">TSPIMessage</span></span>

<span data-ttu-id="ebaf6-104">**Тспимессаже** — это тип перечисления, определяющий набор дополнительных функций [**линивент**](/windows/win32/api/tspi/nc-tspi-lineevent) и [**ФОНИВЕНТ**](/windows/desktop/api/tspi/nc-tspi-phoneevent) , отображаемых в ТСПИ, которые не отображаются в TAPI.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebaf6-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebaf6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebaf6-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_база сообщения \_ тспи</span><span class="sxs-lookup"><span data-stu-id="ebaf6-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="ebaf6-107">Наименьшее число в диапазоне значений сообщений, относящихся к ТСПИ.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="ebaf6-108">Это значение само по себе не имеет смысла, но служит основой для определения других значений.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="ebaf6-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>Строка \_ невкалл</span><span class="sxs-lookup"><span data-stu-id="ebaf6-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="ebaf6-110">Указывает, что новый входящий вызов поступил и вводит его в TAPI.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="ebaf6-111">Это должно быть первое сообщение, отправленное в TAPI для нового входящего вызова.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="ebaf6-112">TAPI возвращает свой непрозрачный идентификатор для вызова в рамках его обработки этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="ebaf6-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>Строка \_ каллдевспеЦифик</span><span class="sxs-lookup"><span data-stu-id="ebaf6-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="ebaf6-114">Указывает, что на устройстве вызова произошло событие конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="ebaf6-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>Строка \_ каллдевспеЦификфеатуре</span><span class="sxs-lookup"><span data-stu-id="ebaf6-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="ebaf6-116">Указывает, что на устройстве вызова произошло событие компонента для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="ebaf6-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
