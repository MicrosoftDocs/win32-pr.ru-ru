---
title: Метки времени пакетов
description: API-интерфейсы отметок времени пакетов поддержки IP предоставляют возможность определить возможность отметок времени для сетевого адаптера и запросить метки времени из сетевого адаптера в виде перекрестных меток времени.
ms.topic: article
ms.date: 01/19/2021
ms.openlocfilehash: 07743473bcb606ccdb86c55f14a3413adf10d73a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110560020"
---
# <a name="packet-timestamping"></a><span data-ttu-id="7deca-103">Метки времени пакетов</span><span class="sxs-lookup"><span data-stu-id="7deca-103">Packet timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="7deca-104">Введение</span><span class="sxs-lookup"><span data-stu-id="7deca-104">Introduction</span></span>

<span data-ttu-id="7deca-105">Многие сетевые карты (сетевые платы или сетевые адаптеры) могут создавать отметки времени на оборудовании при получении или передаче пакетов.</span><span class="sxs-lookup"><span data-stu-id="7deca-105">Many network interface cards (NICs, or network adapters) can generate a timestamp in their hardware whenever a packet is received or transmitted.</span></span> <span data-ttu-id="7deca-106">Метка времени создается с помощью аппаратных часов сетевых карт.</span><span class="sxs-lookup"><span data-stu-id="7deca-106">The timestamp is generated using the NIC's own hardware clock.</span></span> <span data-ttu-id="7deca-107">Эта функция используется в частности протоколом с точностью времени (PTP), который является протоколом синхронизации времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-107">This feature is used in particular by the Precision Time Protocol (PTP), which is a time synchronization protocol.</span></span> <span data-ttu-id="7deca-108">PTP предоставляет возможность использовать такие отметки времени оборудования в самом протоколе.</span><span class="sxs-lookup"><span data-stu-id="7deca-108">PTP makes provision to use such hardware timestamps within the protocol itself.</span></span>

<span data-ttu-id="7deca-109">Метки времени могут, например, использоваться для расчета времени, затраченного на пакет в сетевом стеке компьютера, перед его отправкой или получением от сети.</span><span class="sxs-lookup"><span data-stu-id="7deca-109">The timestamps can, for example, be used to compute the time spent by a packet within the network stack of the machine before being sent to or received from the wire.</span></span> <span data-ttu-id="7deca-110">Эти вычисления можно использовать с помощью PTP для повышения точности синхронизации времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-110">Those calculations can then be used by PTP to improve the accuracy of time synchronization.</span></span> <span data-ttu-id="7deca-111">Поддержка отметок времени пакетов для сетевых адаптеров предназначена для использования в некоторых случаях специально для протокола PTP.</span><span class="sxs-lookup"><span data-stu-id="7deca-111">The packet timestamping support of network adapters is geared sometimes specifically for the PTP protocol.</span></span> <span data-ttu-id="7deca-112">В других случаях предоставляется более общая поддержка.</span><span class="sxs-lookup"><span data-stu-id="7deca-112">In other cases, a more general support is provided.</span></span>

<span data-ttu-id="7deca-113">API-интерфейсы меток времени позволяют Windows поддерживать возможность использования меток оборудования сетевых адаптеров для протокола PTP версии 2.</span><span class="sxs-lookup"><span data-stu-id="7deca-113">Timestamping APIs give Windows the ability to support the hardware timestamping capability of network adapters for the PTP version 2 protocol.</span></span> <span data-ttu-id="7deca-114">В целом функции включают в себя возможность использовать драйверы сетевых адаптеров для поддержки меток времени, а для приложений пользовательского режима — метки времени, связанные с пакетами через [сокеты Windows](/windows/win32/winsock/windows-sockets-start-page-2) (см. раздел о [метке времени Winsock](/windows/win32/winsock/winsock-timestamping)).</span><span class="sxs-lookup"><span data-stu-id="7deca-114">Overall, the features include providing the ability to drivers of network adapters to support timestamps, and for user-mode applications to consume timestamps associated with packets through [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) (see [Winsock timestamping](/windows/win32/winsock/winsock-timestamping)).</span></span> <span data-ttu-id="7deca-115">Кроме того, доступна возможность создания меток времени программного обеспечения, что позволяет сетевому драйверу создавать метки времени в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="7deca-115">In addition, the ability to generate software timestamps is also available, which allows a network driver to generate timestamps in software.</span></span> <span data-ttu-id="7deca-116">Такие метки программного обеспечения создаются драйверами сетевых адаптеров с помощью эквивалента [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="7deca-116">Such software timestamps are generated by NIC drivers using the kernel-mode equivalent of [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).</span></span> <span data-ttu-id="7deca-117">Однако одновременное включение меток времени для оборудования *и* программного обеспечения не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7deca-117">However, having both hardware *and* software timestamps enabled together isn't supported.</span></span>

<span data-ttu-id="7deca-118">В частности, API-интерфейсы поддержки отметок времени пакетов (вспомогательный протокол IP), описанные в этом разделе, предоставляют возможность приложениям пользовательского режима определять возможность отметок времени сетевого адаптера и запрашивать метки времени от сетевого адаптера в виде перекрестных меток времени (описанных ниже).</span><span class="sxs-lookup"><span data-stu-id="7deca-118">In particular, the Internet Protocol Helper (IP Helper) packet timestamping APIs described in this topic provide the ability for user-mode applications to determine the timestamping capability of a network adapter, and to query timestamps from the network adapter in the form of cross timestamps (described below).</span></span>

## <a name="supporting-precision-time-protocol-version-2"></a><span data-ttu-id="7deca-119">Поддержка протокола времени с точностью версии 2</span><span class="sxs-lookup"><span data-stu-id="7deca-119">Supporting Precision Time Protocol version 2</span></span>

<span data-ttu-id="7deca-120">Как уже упоминалось, основная цель поддержки меток времени в Windows — поддержка протокола версии 2 (PTPv2) с поддержкой точности.</span><span class="sxs-lookup"><span data-stu-id="7deca-120">As mentioned, the main goal of timestamping support in Windows is to support the Precision Time Protocol version 2 (PTPv2) protocol.</span></span> <span data-ttu-id="7deca-121">В PTPv2 не все сообщения должны иметь метку времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-121">Within PTPv2, not all messages need a timestamp.</span></span> <span data-ttu-id="7deca-122">В частности, в сообщениях о событиях PTP используются метки времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-122">In particular, PTP event messages do use timestamps.</span></span> <span data-ttu-id="7deca-123">В настоящее время поддержка ограничена PTPv2 по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="7deca-123">Currently, support is scoped to PTPv2 over User Datagram Protocol (UDP).</span></span> <span data-ttu-id="7deca-124">PTP через RAW Ethernet не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7deca-124">PTP over raw ethernet isn't supported.</span></span>

<span data-ttu-id="7deca-125">Отметка времени поддерживается для PTPv2 работы в *2 пошаговом* режиме.</span><span class="sxs-lookup"><span data-stu-id="7deca-125">Timestamping is supported for PTPv2 operating in *2 step* mode.</span></span> <span data-ttu-id="7deca-126">*2 шаг* относится к режиму, в котором фактические метки времени в пакетах PTP не создаются на лету в оборудовании, а извлекаются с оборудования и передаются в виде отдельных сообщений (например, с помощью сообщения об исполнении).</span><span class="sxs-lookup"><span data-stu-id="7deca-126">*2 step* refers to the mode in which the actual timestamps in the PTP packets aren't generated on the fly in the hardware, but are instead retrieved from the hardware and conveyed as separate messages (for example, using a follow-up message).</span></span>

<span data-ttu-id="7deca-127">В сводке для повышения точности синхронизации времени в приложении PTPv2 можно использовать API-интерфейсы отметок времени пакетов поддержки протокола Интернета (вспомогательный протокол IP), а также поддержку меток времени Winsock.</span><span class="sxs-lookup"><span data-stu-id="7deca-127">In summary, you can use the Internet Protocol Helper (IP Helper) packet timestamping APIs, together with Winsock's timestamping support, in a PTPv2 application to improve its time synchronization accuracy.</span></span>

## <a name="retrieving-the-timestamping-capabilities-of-a-network-adapter"></a><span data-ttu-id="7deca-128">Получение возможностей отметок времени сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="7deca-128">Retrieving the timestamping capabilities of a network adapter</span></span>

<span data-ttu-id="7deca-129">Приложение, такое как служба синхронизации времени PTP, должно определять возможность отметок времени для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="7deca-129">An application such as a PTP time synchronization service needs to determine the timestamping capability of a network adapter.</span></span> <span data-ttu-id="7deca-130">Используя полученные возможности, приложение может определить, нужно ли использовать метки времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-130">Using the retrieved capabilities, the application can then decide whether or not it wants to use timestamps.</span></span>

<span data-ttu-id="7deca-131">Даже если *сетевой адаптер поддерживает* метки времени, по умолчанию он должен оставаться отключенным.</span><span class="sxs-lookup"><span data-stu-id="7deca-131">Even if a network adapter *does* support timestamps, it's required to keep the ability turned off by default.</span></span> <span data-ttu-id="7deca-132">При этом адаптер включает метки времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-132">An adapter turns on timestamping when instructed to do so.</span></span> <span data-ttu-id="7deca-133">Windows предоставляет API-интерфейсы для приложения, чтобы получить возможности оборудования, а также какие возможности включены.</span><span class="sxs-lookup"><span data-stu-id="7deca-133">Windows provides APIs for an application to retrieve the hardware's capability, as well as which capabilities are turned on.</span></span>

<span data-ttu-id="7deca-134">Чтобы получить поддерживаемые возможности отметок времени сетевого адаптера, вызовите функцию [**жетинтерфацесуппортедтиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) , предоставляющую локально уникальный идентификатор (LUID) сетевого адаптера, а затем возвратите поддерживаемые возможности отметки времени в форме объекта [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="7deca-134">To retrieve the supported timestamp capabilities of a network adapter, you call the [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the supported timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="7deca-135">Код, возвращенный из **жетинтерфацесуппортедтиместампкапабилитиес** , указывает, успешно ли был выполнен вызов, а также было ли получено заполненное **INTERFACE_TIMESTAMP_CAPABILITIES** значение.</span><span class="sxs-lookup"><span data-stu-id="7deca-135">The code returned from **GetInterfaceSupportedTimestampCapabilities** indicates whether or not the call succeeded, and whether or not a populated **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="7deca-136">Чтобы получить текущие включенные возможности отметки времени для сетевого адаптера, вызовите функцию [**жетинтерфацеактиветиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) , предоставляющую локально уникальный идентификатор (LUID) сетевого адаптера, а затем возвратите включенные возможности отметок времени в форме объекта [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="7deca-136">To retrieve the currently enabled timestamp capabilities of a network adapter, you call the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the enabled timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="7deca-137">Опять же, код, возвращенный из **жетинтерфацеактиветиместампкапабилитиес** , указывает на успешное выполнение или ошибку, а также на то, было ли получено допустимое значение **INTERFACE_TIMESTAMP_CAPABILITIES** .</span><span class="sxs-lookup"><span data-stu-id="7deca-137">Again, the code returned from **GetInterfaceActiveTimestampCapabilities** indicates success or failure, and whether or not a valid **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="7deca-138">Сетевые адаптеры могут поддерживать различные возможности работы с метками времени.</span><span class="sxs-lookup"><span data-stu-id="7deca-138">Network adapters can support a variety of timestamping capabilities.</span></span> <span data-ttu-id="7deca-139">Например, некоторые адаптеры могут отметку времени каждого пакета во время отправки и получения, а другие поддерживают только пакеты PTPv2.</span><span class="sxs-lookup"><span data-stu-id="7deca-139">For example, some adapters can timestamp every packet during send and receive, while others support only PTPv2 packets.</span></span> <span data-ttu-id="7deca-140">Структура [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) описывает конкретные возможности, поддерживаемые сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="7deca-140">The [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) structure describes the exact capabilities that a network adapter supports.</span></span>

## <a name="retrieving-cross-timestamps-from-a-network-adapter"></a><span data-ttu-id="7deca-141">Получение перекрестных меток времени из сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="7deca-141">Retrieving cross timestamps from a network adapter</span></span>

<span data-ttu-id="7deca-142">При использовании аппаратных отметок времени приложение PTP должно установить связь (например, с помощью соответствующих математических методов) между аппаратными часами сетевого адаптера и системными часами.</span><span class="sxs-lookup"><span data-stu-id="7deca-142">When using hardware timestamps, a PTP application needs to establish a relation (for example, by using appropriate mathematical techniques) between the hardware clock of the network adapter and a system clock.</span></span> <span data-ttu-id="7deca-143">Это необходимо для того, чтобы значение, представляющее время в одной единице времени, можно было преобразовать в единицу другого часового пояса.</span><span class="sxs-lookup"><span data-stu-id="7deca-143">This is necessary so that a value representing a time in one clock's unit can be converted into another clock's unit.</span></span> <span data-ttu-id="7deca-144">Для этой цели предоставляются различные метки времени, и приложение может периодически выполнять выборку меток времени, чтобы установить такое отношение.</span><span class="sxs-lookup"><span data-stu-id="7deca-144">Cross timestamps are provided for this purpose, and your application can sample cross timestamps periodically in order to establish such a relation.</span></span>

<span data-ttu-id="7deca-145">Для этого вызовите функцию [**каптуреинтерфацехардварекросстиместамп**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) , предоставляющую локально уникальный идентификатор (LUID) сетевого адаптера, а затем возвратите отметку времени из сетевого адаптера в форме объекта [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) .</span><span class="sxs-lookup"><span data-stu-id="7deca-145">To do that, call the [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the timestamp from the network adapter in the form of an [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) object.</span></span>

## <a name="timestamp-capability-change-notifications"></a><span data-ttu-id="7deca-146">Уведомления об изменении возможностей метки времени</span><span class="sxs-lookup"><span data-stu-id="7deca-146">Timestamp capability change notifications</span></span>

<span data-ttu-id="7deca-147">Чтобы получать уведомления о возможностях изменения отметок времени для сетевого адаптера, вызовите функцию [**регистеринтерфацетиместампконфигчанже**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) , предоставив указатель на функцию обратного вызова, которую вы реализовали вместе с дополнительным контекстом, выделенным вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="7deca-147">To be notified should the timestamp capabilities for a network adapter change, call the [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) function, providing a pointer to the callback function that you've implemented, together with an optional caller-allocated context.</span></span>

<span data-ttu-id="7deca-148">**Регистеринтерфацетиместампконфигчанже** возвращает маркер, который впоследствии можно передать в [**унрегистеринтерфацетиместампконфигчанже**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) , чтобы отменить регистрацию функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7deca-148">**RegisterInterfaceTimestampConfigChange** returns a handle that you can subsequently pass to [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) in order to unregister your callback function.</span></span>

## <a name="code-example-1mdashretrieving-timestamp-capabilities-and-cross-timestamps"></a><span data-ttu-id="7deca-149">Пример кода 1. &mdash; Извлечение возможностей отметок времени и перекрестных меток времени</span><span class="sxs-lookup"><span data-stu-id="7deca-149">Code example 1&mdash;retrieving timestamp capabilities and cross timestamps</span></span>

```c
// main.cpp in a Console App project.

#include <stdio.h>
#include <winsock2.h>
#include <iphlpapi.h>
#pragma comment(lib, "Iphlpapi")

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv4(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv6(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// This function checks and returns the supported timestamp capabilities for an interface for
// a PTPv2 application
SupportedTimestampType
CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities;
    SupportedTimestampType supportedType = TimestampTypeNone;

    result = GetInterfaceActiveTimestampCapabilities(
                 &interfaceLuid,
                 &timestampCapabilities);
    if (result != NO_ERROR)
    {
        printf("Error retrieving hardware timestamp capabilities: %d\n", result);
        goto Exit;
    }

    if (IsPTPv2HardwareTimestampingSupportedForIPv4(&timestampCapabilities) &&
        IsPTPv2HardwareTimestampingSupportedForIPv6(&timestampCapabilities))
    {
        supportedType = TimestampTypeHardware;
        goto Exit;
    }
    else
    {
        if ((timestampCapabilities.SoftwareCapabilities.AllReceive) &&
            ((timestampCapabilities.SoftwareCapabilities.AllTransmit) ||
             (timestampCapabilities.SoftwareCapabilities.TaggedTransmit)))
        {
            supportedType = TimestampTypeSoftware;
        }
    }

Exit:
    return supportedType;
}

// Helper function which does the correlation between hardware and system clock
// using mathematical techniques
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// An application would call this function periodically to gather a set 
// of matching timestamps for use in converting hardware timestamps to
// system timestamps
DWORD
RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp;

    result = CaptureInterfaceHardwareCrossTimestamp(
                 &interfaceLuid,
                 &crossTimestamp);
    if (result != NO_ERROR)
    {
        printf("Error retrieving cross timestamp for the interface: %d\n", result);
        goto Exit;
    }

    // Process crossTimestamp further to create a relation between the hardware clock
    // of the NIC and the QPC values using appropriate mathematical techniques
    ComputeCorrelationOfHardwareAndSystemTimestamps(&crossTimestamp);

Exit:
    return result;
}

int main()
{
}
```

## <a name="code-example-2mdashregistering-for-timestamp-capability-change-notifications"></a><span data-ttu-id="7deca-150">Пример кода 2. &mdash; Регистрация для получения уведомлений об изменении возможностей метки времени</span><span class="sxs-lookup"><span data-stu-id="7deca-150">Code example 2&mdash;registering for timestamp capability change notifications</span></span>

<span data-ttu-id="7deca-151">В этом примере показано, как приложение может использовать метки времени в конце.</span><span class="sxs-lookup"><span data-stu-id="7deca-151">This example shows how your application could use timestamps end to end.</span></span>

```c
// main.cpp in a Console App project.

#include <stdlib.h>
#include <stdio.h>
#include <winsock2.h>
#include <mswsock.h>
#include <iphlpapi.h>
#include <mstcpip.h>
#pragma comment(lib, "Ws2_32")
#pragma comment(lib, "Iphlpapi")

// Globals and function declarations used by the application.
// The sample functions and skeletons demonstrate:
// - Checking timestamp configuration for an interface to determine if timestamping can be used
// - If timestamping is enabled, starts tracking changes in timestamp configuration
// - Performing correlation between hardware and system timestamps using cross timestamps
//   on a separate thread depending on the timestamp type configured
// - Receiving a packet and computing the latency between when the timestamp
//   was generated on packet reception, and when the packet was received by
//   the application through the socket
// The sample tries to demonstrate how an application could use timestamps. It is not thread safe 
// and does not do exhaustive error checking.
// Lot of the functions are provided as skeletons, or only declared and invoked
// but are not defined. It is up to
// the application to implement these suitably.

// An application could use the functions below by e.g.
// - Call InitializeTimestampingForInterface for the interface it wants to track for timestamping capability.
// - Call EstimateReceiveLatency to estimate the receive latency of a packet depending on the timestamp 
//   type configured for the interface.

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// interfaceBeingTracked is the interface the PTPv2 application
// intends to use for timestamping purpose.
wchar_t* interfaceBeingTracked;

// The active timestamping type determined for
// interfaceBeingTracked.
SupportedTimestampType timestampTypeEnabledForInterface;

HANDLE correlationThread;
HANDLE threadStopEvent;
HIFTIMESTAMPCHANGE TimestampChangeNotificationHandle = NULL;

// Function from sample above to check if an interface supports timestamping for PTPv2.
SupportedTimestampType CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid);

// Function from sample above to retrieve cross timestamps and process them further.
DWORD RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid);

// Helper function which registers for timestamp configuration changes.
DWORD RegisterTimestampChangeNotifications();

// Callback function which is invoked when timestamp configuration changes
// for some network interface.
INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK TimestampConfigChangeCallback;

// Function which does the correlation between hardware and system clock
// using mathematical techniques. It is periodically invoked and provided
// a sample of cross timestamp to compute a correlation.
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// Helper function which converts a hardware timestamp from the NIC clock
// to system timestamp (QPC) values. It is assumed that this works together
// with the ComputeCorrelationOfHardwareAndSystemTimestamps function
// to derive the correlation.
ULONG64 ConvertHardwareTimestampToQpc(ULONG64 HardwareTimestamp);

// Start function of thread which periodically samples
// cross timestamps to correlate hardware and software timestamps.
DWORD WINAPI CorrelateHardwareAndSystemTimestamps(LPVOID);

// Helper function which starts a new thread at CorrelateHardwareAndSystemTimestamps.
DWORD StartCorrelatingHardwareAndSytemTimestamps();

// Helper function which restarts correlation when some change is detected.
DWORD RestartCorrelatingHardwareAndSystemTimestamps();

// Stops the correlation thread.
DWORD StopCorrelatingHardwareAndSystemTimestamps();

DWORD
FindInterfaceFromFriendlyName(wchar_t* friendlyName, NET_LUID* interfaceLuid)
{
    DWORD result = 0;
    ULONG flags = 0;
    ULONG outBufLen = 0;
    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    PIP_ADAPTER_ADDRESSES currentAddresses = NULL;

    result = GetAdaptersAddresses(0,
        flags,
        NULL,
        pAddresses,
        &outBufLen);
    if (result == ERROR_BUFFER_OVERFLOW)
    {
        pAddresses = (PIP_ADAPTER_ADDRESSES)malloc(outBufLen);

        result = GetAdaptersAddresses(0,
            flags,
            NULL,
            pAddresses,
            &outBufLen);
        if (result != NO_ERROR)
        {
            goto Done;
        }
    }
    else if (result != NO_ERROR)
    {
        goto Done;
    }

    currentAddresses = pAddresses;
    while (currentAddresses != NULL)
    {
        if (wcscmp(friendlyName, currentAddresses->FriendlyName) == 0)
        {
            result = ConvertInterfaceIndexToLuid(currentAddresses->IfIndex, interfaceLuid);
            goto Done;
        }

        currentAddresses = currentAddresses->Next;
    }

    result = ERROR_NOT_FOUND;

Done:

    if (pAddresses != NULL)
    {
        free(pAddresses);
    }

    return result;
}

// This function checks if an interface is suitable for
// timestamping for PTPv2. If so, it registers for timestamp
// configuration changes and initializes some globals.
// If hardware  timestamping is enabled it also starts
// correlation thread.
DWORD
InitializeTimestampingForInterface(wchar_t* friendlyName)
{
    DWORD error;
    SupportedTimestampType supportedType = TimestampTypeNone;

    NET_LUID interfaceLuid;

    error = FindInterfaceFromFriendlyName(friendlyName, &interfaceLuid);
    if (error != 0)
    {
        return error;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if (supportedType != TimestampTypeNone)
    {
        error = RegisterTimestampChangeNotifications();
        if (error != NO_ERROR)
        {
            return error;
        }

        if (supportedType == TimestampTypeHardware)
        {
            threadStopEvent = CreateEvent(
                NULL,
                FALSE,
                FALSE,
                NULL
            );
            if (threadStopEvent == NULL)
            {
                return GetLastError();
            }            

            error = StartCorrelatingHardwareAndSytemTimestamps();
            if (error != 0)
            {
                return error;
            }
        }

        interfaceBeingTracked = friendlyName;
        timestampTypeEnabledForInterface = supportedType;

        return error;
    }

    return ERROR_NOT_SUPPORTED;
}

DWORD
RegisterTimestampChangeNotifications()
{
    DWORD retcode = NO_ERROR;

    // Register with NULL context
    retcode = RegisterInterfaceTimestampConfigChange(TimestampConfigChangeCallback, NULL, &TimestampChangeNotificationHandle);
    if (retcode != NO_ERROR)
    {
        printf("Error when calling RegisterIfTimestampConfigChange %d\n", retcode);
    }

    return retcode;
}

// The callback invoked when change in some interface’s timestamping configuration
// happens. The callback takes appropriate action based on the new capability of the
// interface. The callback assumes that there is only 1 NIC. If multiple NICs are being
// tracked for timestamping then the application would need to check all of them.
VOID
WINAPI
TimestampConfigChangeCallback(
    _In_ PVOID /*CallerContext*/
    )
{
    SupportedTimestampType supportedType;

    NET_LUID interfaceLuid;
    DWORD error;

    error = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (error != NO_ERROR)
    {
        if (timestampTypeEnabledForInterface == TimestampTypeHardware)
        {
            StopCorrelatingHardwareAndSystemTimestamps();
            timestampTypeEnabledForInterface = TimestampTypeNone;
        }
        return;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if ((supportedType == TimestampTypeHardware) &&
        (timestampTypeEnabledForInterface == TimestampTypeHardware))
    {
        // NIC could have been restarted, restart the correlation between hardware and 
        // system timestamps.
        RestartCorrelatingHardwareAndSystemTimestamps();
    }
    else if (supportedType == TimestampTypeHardware)
    {
        // Start thread correlating hardware and software timestamps
        StartCorrelatingHardwareAndSytemTimestamps();
    }
    else if (supportedType != TimestampTypeHardware)
    {
        // Hardware timestamps are not enabled, stop correlation
        StopCorrelatingHardwareAndSystemTimestamps();
    }

    timestampTypeEnabledForInterface = supportedType;
}

DWORD 
StartCorrelatingHardwareAndSytemTimestamps()
{
    // Create a new thread which starts at CorrelateHardwareAndSoftwareTimestamps
    correlationThread = CreateThread(
        NULL,
        0,
        CorrelateHardwareAndSystemTimestamps,
        NULL,
        0,
        NULL); 

    if (correlationThread == NULL)
    {
        return GetLastError();
    }
}

// Thread which periodically invokes functions to 
// sample cross timestamps and use them to compute
// correlation between hardware and system timestamps.
DWORD WINAPI
CorrelateHardwareAndSystemTimestamps(LPVOID /*lpParameter*/)
{
    DWORD error;
    NET_LUID interfaceLuid;
    DWORD result;

    result = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (result != 0)
    {
        return result;
    }

    while (TRUE)
    {
        error = RetrieveAndProcessCrossTimestamp(interfaceLuid);

        // Sleep and repeat till the thread gets a signal to stop
        result = WaitForSingleObject(threadStopEvent, 5000);
        if (result != WAIT_TIMEOUT)
        {
            if (result == WAIT_OBJECT_0)
            {
                return 0;
            }
            else if (result == WAIT_FAILED)            
            {
                return GetLastError();
            }

            return result;
        }
    }
}

DWORD
StopCorrelatingHardwareAndSystemTimestamps()
{
    SetEvent(threadStopEvent);
    return 0;
}

// Function which receives a packet and estimates the latency between the 
// point at which receive timestamp (of appropriate type) was generated
// and when the packet was received in the app through the socket.
// The sample assumes that there is only 1 NIC in the system. This is the NIC which is tracked through
// interfaceBeingTracked for correlation purpose, and through which packets are being
// received by the socket.
// The recvmsg parameter is of type LPFN_WSARECVMSG and an application can
// retrieve it by issuing WSAIoctl
// with SIO_GET_EXTENSION_FUNCTION_POINTER control
// and WSAID_WSARECVMSG. Please refer to msdn.
void EstimateReceiveLatency(SOCKET sock, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;
    ULONG64 packetReceivedTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.Flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    if (timestampTypeEnabledForInterface != TimestampTypeNone)
    {
        // Capture system timestamp (QPC) upon message reception.
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;

        printf("received packet\n");

        // Look for socket rx timestamp returned via control message.
        BOOLEAN retrievedTimestamp = FALSE;
        PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
        while (cmsg != NULL)
        {
            if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP)
            {
                socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
                retrievedTimestamp = TRUE;
                break;
            }
            cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
        }

        if (retrievedTimestamp)
        {
            // Compute socket receive path latency.
            LARGE_INTEGER clockFrequency;
            ULONG64 elapsedMicroseconds;

            if (timestampTypeEnabledForInterface == TimestampTypeHardware)
            {
                packetReceivedTimestamp = ConvertHardwareTimestampToQpc(socketTimestamp);
            }
            else
            {
                packetReceivedTimestamp = socketTimestamp;
            }
        
            QueryPerformanceFrequency(&clockFrequency);

            // Compute socket receive path latency.
            elapsedMicroseconds = appLevelTimestamp - packetReceivedTimestamp;
            elapsedMicroseconds *= 1000000;
            elapsedMicroseconds /= clockFrequency.QuadPart;
            printf("RX latency estimation: %lld microseconds\n",
                 elapsedMicroseconds);
        }
        else
        {
            printf("failed to retrieve RX timestamp\n");
        }
    }
}

int main()
{
}
```
