---
description: Квалификаторы содержат зависящую от реализации контекстную информацию и свойства транспорта, определяющие, как поставщик SNMP обращается к агенту SNMP. Ниже перечислены квалификаторы, уникальные для поставщика SNMP.
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: Квалификаторы, характерные для поставщика SNMP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811405"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="84baf-104">Квалификаторы, характерные для поставщика SNMP</span><span class="sxs-lookup"><span data-stu-id="84baf-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="84baf-105">Квалификаторы содержат зависящую от реализации контекстную информацию и свойства транспорта, определяющие, как поставщик SNMP обращается к агенту SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="84baf-106">Ниже перечислены квалификаторы, уникальные для поставщика SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="84baf-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**ажентаддресс**</span><span class="sxs-lookup"><span data-stu-id="84baf-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-108">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="84baf-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84baf-109">Адрес транспорта, связанный с агентом SNMP, например IP-адрес или DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="84baf-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="84baf-110">Необходимо задать для **ажентаддресс** допустимый адрес узла одноадресной рассылки или имя узла домена, которое можно разрешить с помощью процесса разрешения имен доменов операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84baf-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="84baf-111">**Ажентаддресс** не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84baf-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**ажентфловконтролвиндовсизе**</span><span class="sxs-lookup"><span data-stu-id="84baf-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-113">Тип данных: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="84baf-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="84baf-114">Максимальное количество параллельно необработанных SNMP-запросов, которые могут быть отправлены этому агенту, пока ответ еще не получен.</span><span class="sxs-lookup"><span data-stu-id="84baf-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="84baf-115">Запрос SNMP считается ожидающим, пока не будет получен ответ PDU или истекло время его ожидания. Большой размер окна обычно повышает производительность, но некоторые агенты могут не работать при большой нагрузке.</span><span class="sxs-lookup"><span data-stu-id="84baf-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="84baf-116">**Ажентфловконтролвиндовсизе** может иметь значение 0, чтобы указать неограниченный размер окна или целое число от 1 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="84baf-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="84baf-117">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="84baf-117">The default value is 10.</span></span> <span data-ttu-id="84baf-118">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**ажентреадкоммунитинаме**</span><span class="sxs-lookup"><span data-stu-id="84baf-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-120">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="84baf-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84baf-121">Строка октета переменной длины, используемая агентом SNMP для проверки подлинности блока данных протокола SNMP во время операции чтения (следующие запросы SNMP GET и GET).</span><span class="sxs-lookup"><span data-stu-id="84baf-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="84baf-122">Имя сообщества должно быть сопоставлено с строкой Юникода и содержать только буквенно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="84baf-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="84baf-123">Значение по умолчанию — Public.</span><span class="sxs-lookup"><span data-stu-id="84baf-123">The default value is public.</span></span> <span data-ttu-id="84baf-124">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**ажентретрикаунт**</span><span class="sxs-lookup"><span data-stu-id="84baf-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-126">Тип данных: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="84baf-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="84baf-127">Количество повторных попыток одного SNMP-запроса при отсутствии ответа от агента SNMP до того, как запрос будет считаться неудачным.</span><span class="sxs-lookup"><span data-stu-id="84baf-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="84baf-128">Для **ажентретрикаунт** должно быть задано целое число от 0 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="84baf-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="84baf-129">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="84baf-129">The default value is 1.</span></span> <span data-ttu-id="84baf-130">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**ажентретритимеаут**</span><span class="sxs-lookup"><span data-stu-id="84baf-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-132">Тип данных: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="84baf-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="84baf-133">Время в миллисекундах, по истечении которого будет считаться, что единица данных протокола SNMP была удалена.</span><span class="sxs-lookup"><span data-stu-id="84baf-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="84baf-134">Число миллисекунд, в течение которых ожидается ответ на SNMP-запрос, отправленный агенту SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="84baf-135">Для **ажентретритимеаут** должно быть задано целое число от 0 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="84baf-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="84baf-136">Значение по умолчанию — 500.</span><span class="sxs-lookup"><span data-stu-id="84baf-136">The default value is 500.</span></span> <span data-ttu-id="84baf-137">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**ажентснмпверсион**</span><span class="sxs-lookup"><span data-stu-id="84baf-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-139">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="84baf-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84baf-140">Версия протокола SNMP, используемая при взаимодействии с агентом SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="84baf-141">В настоящее время допустимыми значениями являются 1 (для CLR) и 2C (для SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="84baf-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="84baf-142">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="84baf-142">The default value is 1.</span></span> <span data-ttu-id="84baf-143">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**аженттранспорт**</span><span class="sxs-lookup"><span data-stu-id="84baf-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-145">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="84baf-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84baf-146">Транспортный протокол, используемый для взаимодействия с агентом SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="84baf-147">В настоящее время единственными допустимыми значениями являются протоколы IP и Internet Packet Exchange (IPX).</span><span class="sxs-lookup"><span data-stu-id="84baf-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="84baf-148">Значение по умолчанию — IP.</span><span class="sxs-lookup"><span data-stu-id="84baf-148">The default value is IP.</span></span> <span data-ttu-id="84baf-149">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**ажентварбиндсперпду**</span><span class="sxs-lookup"><span data-stu-id="84baf-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-151">Тип данных: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="84baf-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="84baf-152">Максимальное число привязок переменных, содержащихся в одном PDU SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="84baf-153">Каждый SNMP-запрос, отправленный агенту SNMP, содержит одну или несколько переменных SNMP.</span><span class="sxs-lookup"><span data-stu-id="84baf-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="84baf-154">Этот параметр задает максимальное число переменных, которые могут быть добавлены в один запрос.</span><span class="sxs-lookup"><span data-stu-id="84baf-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="84baf-155">**Ажентварбиндсперпду** может иметь значение 0 (ноль), чтобы реализация могла определить оптимальные привязки переменных или целое число от 1 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="84baf-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="84baf-156">Обратите внимание, что хотя увеличение этого значения может повысить производительность, некоторые агенты и сети не могут работать с полученным запросом.</span><span class="sxs-lookup"><span data-stu-id="84baf-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="84baf-157">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="84baf-157">The default value is 10.</span></span> <span data-ttu-id="84baf-158">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="84baf-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**ажентвритекоммунитинаме**</span><span class="sxs-lookup"><span data-stu-id="84baf-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="84baf-160">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="84baf-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84baf-161">Строка октета переменной длины, используемая агентом SNMP для проверки подлинности блока данных протокола SNMP во время операции записи (запрос SNMP SET).</span><span class="sxs-lookup"><span data-stu-id="84baf-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="84baf-162">Имя сообщества должно быть сопоставлено с строкой Юникода и содержать только буквенно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="84baf-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="84baf-163">Значение по умолчанию — Public.</span><span class="sxs-lookup"><span data-stu-id="84baf-163">The default value is public.</span></span> <span data-ttu-id="84baf-164">Этот квалификатор является необязательным.</span><span class="sxs-lookup"><span data-stu-id="84baf-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84baf-165">Требования</span><span class="sxs-lookup"><span data-stu-id="84baf-165">Requirements</span></span>



| <span data-ttu-id="84baf-166">Требование</span><span class="sxs-lookup"><span data-stu-id="84baf-166">Requirement</span></span> | <span data-ttu-id="84baf-167">Значение</span><span class="sxs-lookup"><span data-stu-id="84baf-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="84baf-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84baf-168">Minimum supported client</span></span><br/> | <span data-ttu-id="84baf-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84baf-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="84baf-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84baf-170">Minimum supported server</span></span><br/> | <span data-ttu-id="84baf-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84baf-171">Windows Server 2008</span></span><br/> |



 

 




