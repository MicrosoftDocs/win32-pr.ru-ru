---
description: '\_Константы побитового флага линебеарермоде описывают различные режимы носителя вызова.'
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Константы LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689390"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="5fe81-103">\_Константы линебеарермоде</span><span class="sxs-lookup"><span data-stu-id="5fe81-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="5fe81-104">Константы побитового флага **линебеарермоде \_** описывают различные режимы носителя вызова.</span><span class="sxs-lookup"><span data-stu-id="5fe81-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="5fe81-105">Когда приложение выполняет вызов, оно может запросить конкретный режим носителя.</span><span class="sxs-lookup"><span data-stu-id="5fe81-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="5fe81-106">Эти режимы используются для выбора определенного качества обслуживания для запрошенного подключения из базовой телефонной сети.</span><span class="sxs-lookup"><span data-stu-id="5fe81-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="5fe81-107">Режимы носителя, доступные в данной строке, являются возможностью устройства в строке.</span><span class="sxs-lookup"><span data-stu-id="5fe81-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="5fe81-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**ЛИНЕБЕАРЕРМОДЕ \_ алтспичдата**</span><span class="sxs-lookup"><span data-stu-id="5fe81-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-109">Альтернативная перенаправление речи или неограниченных данных в одном вызове (ISDN).</span><span class="sxs-lookup"><span data-stu-id="5fe81-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**\_данные линебеарермоде**</span><span class="sxs-lookup"><span data-stu-id="5fe81-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-111">Неограниченное перемещение данных при вызове.</span><span class="sxs-lookup"><span data-stu-id="5fe81-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="5fe81-112">Скорость передачи данных указывается отдельно.</span><span class="sxs-lookup"><span data-stu-id="5fe81-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**ЛИНЕБЕАРЕРМОДЕ \_ многократное**</span><span class="sxs-lookup"><span data-stu-id="5fe81-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-114">Режим многократное, определенный ISDN.</span><span class="sxs-lookup"><span data-stu-id="5fe81-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**ЛИНЕБЕАРЕРМОДЕ \_ нонкаллсигналинг**</span><span class="sxs-lookup"><span data-stu-id="5fe81-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-116">Это соответствует сигнальному соединению, не связанному с вызовом, от приложения к поставщику услуг или коммутатору (который рассматривается TAPI как поток мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="5fe81-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**\_транзитный линебеарермоде**</span><span class="sxs-lookup"><span data-stu-id="5fe81-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-118">При активации вызова в ЛИНЕБЕАРЕРМОДЕ \_ passthrough поставщик услуг предоставляет прямой доступ к подключенному оборудованию для управления приложением.</span><span class="sxs-lookup"><span data-stu-id="5fe81-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="5fe81-119">Этот режим используется главным образом приложениями, которым необходимо временное прямое управление асинхронными модемами, доступ к которым осуществляется через [функции связи](/windows/desktop/DevIO/communications-functions), для настройки или использования специальных функций, которые не поддерживаются поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="5fe81-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**ЛИНЕБЕАРЕРМОДЕ \_ рестриктеддата**</span><span class="sxs-lookup"><span data-stu-id="5fe81-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-121">Служба носителя для цифровых данных, в которой только семь младших бит каждого октета могут содержать данные пользователя (например, для службы Switchd 56kbit/s).</span><span class="sxs-lookup"><span data-stu-id="5fe81-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**ЛИНЕБЕАРЕРМОДЕ \_ речь**</span><span class="sxs-lookup"><span data-stu-id="5fe81-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-123">Это соответствует передаче речи G. 711 в вызове.</span><span class="sxs-lookup"><span data-stu-id="5fe81-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="5fe81-124">Сеть может использовать такие методы обработки, как аналоговая передача, отмена эха, сжатие и распаковка.</span><span class="sxs-lookup"><span data-stu-id="5fe81-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="5fe81-125">Битовая целостность не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="5fe81-125">Bit integrity is not assured.</span></span> <span data-ttu-id="5fe81-126">Речь не поддерживает типы мультимедиа для факсов и модемов.</span><span class="sxs-lookup"><span data-stu-id="5fe81-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fe81-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**ЛИНЕБЕАРЕРМОДЕ \_ голоса**</span><span class="sxs-lookup"><span data-stu-id="5fe81-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5fe81-128">Это обычная служба носителя с аналоговым голосовым стандартом 3,1 кГц.</span><span class="sxs-lookup"><span data-stu-id="5fe81-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="5fe81-129">Битовая целостность не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="5fe81-129">Bit integrity is not assured.</span></span> <span data-ttu-id="5fe81-130">Голосовое сообщение может поддерживать типы мультимедиа факсов и модемов.</span><span class="sxs-lookup"><span data-stu-id="5fe81-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fe81-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fe81-131">Remarks</span></span>

<span data-ttu-id="5fe81-132">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="5fe81-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="5fe81-133">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="5fe81-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="5fe81-134">Обратите внимание, что режим носителя и тип мультимедиа являются разными понятиями.</span><span class="sxs-lookup"><span data-stu-id="5fe81-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="5fe81-135">Режим носителя вызова указывает на качество телефонного подключения, которое предоставляется в основном в сети.</span><span class="sxs-lookup"><span data-stu-id="5fe81-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="5fe81-136">Тип носителя вызова указывает на тип информационного потока, который передается через этот вызов.</span><span class="sxs-lookup"><span data-stu-id="5fe81-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="5fe81-137">Факсы группы 3 или модемы данных — это типы мультимедиа, использующие вызов с режимом носителя 3,1 кГц.</span><span class="sxs-lookup"><span data-stu-id="5fe81-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe81-138">Требования</span><span class="sxs-lookup"><span data-stu-id="5fe81-138">Requirements</span></span>



| <span data-ttu-id="5fe81-139">Требование</span><span class="sxs-lookup"><span data-stu-id="5fe81-139">Requirement</span></span> | <span data-ttu-id="5fe81-140">Значение</span><span class="sxs-lookup"><span data-stu-id="5fe81-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5fe81-141">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5fe81-141">TAPI version</span></span><br/> | <span data-ttu-id="5fe81-142">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5fe81-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5fe81-143">Header</span><span class="sxs-lookup"><span data-stu-id="5fe81-143">Header</span></span><br/>       | <dl> <span data-ttu-id="5fe81-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe81-144"><dt>Tapi.h</dt></span></span> </dl> |



 

