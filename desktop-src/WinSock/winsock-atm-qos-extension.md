---
description: В этом разделе описывается структура качества обслуживания, зависящая от протокола (QOS) для ATM, которая содержится в поле ПровидерспеЦифик структуры QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Расширение службы Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144935"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="e7fc4-103">Расширение службы Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="e7fc4-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="e7fc4-104">В этом разделе описывается структура качества обслуживания, зависящая от протокола ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) для ATM, которая содержится в поле [провидерспеЦифик](/previous-versions/aa374467(v=vs.80)) структуры **QoS** .</span><span class="sxs-lookup"><span data-stu-id="e7fc4-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="e7fc4-105">Обратите внимание, что использование этой структуры **QoS** , относящейся к ATM, является необязательным для клиентов Windows Sockets 2, а поставщик услуг ATM должен сопоставлять универсальную структуру [**фловспек**](/windows/win32/api/qos/ns-qos-flowspec) с соответствующими информационными элементами Q. 2931.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="e7fc4-106">Однако если указаны Универсальная структура **фловспек** и структура **QoS** , относящаяся к ATM, то значение, указанное в структуре **QoS** , относящейся к ATM, должно иметь приоритет при наличии конфликтов.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="e7fc4-107">Дополнительные сведения о подготовке к качеству обслуживания и структуре **фловспек** см. в разделе Спецификация API Windows Sockets 2 2,7.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="e7fc4-108">Зависящая от протокола структура [**обслуживания**](/windows/win32/api/winsock2/ns-winsock2-qos) для ATM представляет собой объединение структур информационного элемента Q. 2931 Information (IE), которые определены в следующем тексте.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="e7fc4-109">Если в приложении отсутствует IE, заданное в некотором задании UNI 3. x, поставщик услуг должен вставить разумное значение по умолчанию, принимая во внимание структуру [**фловспек**](/windows/win32/api/qos/ns-qos-flowspec) , если это применимо.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="e7fc4-110">Обработка повторяющихся спецификаций зависит от самого ОБОЗРЕВАТЕЛЯ.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="e7fc4-111">Если обозреватель Internet Explorer повторяется и его можно повторить в соответствии со спецификацией ATM Forum UNI, поставщик должен правильно обрабатывать его.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="e7fc4-112">В этом случае Order в списке определяет порядок предпочтения, и элементы, показываемые ранее в списке, являются более предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="e7fc4-113">Если обозреватель Internet Explorer повторяется и это не разрешено в соответствии со спецификацией ATM Forum UNI, поставщик может либо отдать запрос от клиента (предпочтительный вариант), либо использовать последний IE этого типа.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="e7fc4-114">Каждая отдельная структура IE форматируется следующим образом и определяется полем **иетипе** :</span><span class="sxs-lookup"><span data-stu-id="e7fc4-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="e7fc4-115">Допустимые значения для поля **иетипе** определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e7fc4-115">Legal values for the **IEType** field are defined as:</span></span>

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

<span data-ttu-id="e7fc4-116">Поле **IE** перемещается определенной структурой IE, а поле **иеленгс** — общей длиной в байтах структуры IE, включая поля **иетипе** и **иеленгс** .</span><span class="sxs-lookup"><span data-stu-id="e7fc4-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="e7fc4-117">Семантика и допустимые значения для каждого элемента в этих структурах IE относятся к спецификации ATM UNI 3. x.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="e7fc4-118">\_ \_ Отсутствующее поле SAP может использоваться для элементов, которые являются необязательными для данной структуры IE, в соответствии со СПЕЦИФИКАЦИЕЙ ATM UNI 3. x.</span><span class="sxs-lookup"><span data-stu-id="e7fc4-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
