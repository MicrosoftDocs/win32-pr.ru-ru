---
description: Содержит подробные сведения о интерфейсе, который требуется клиенту RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: Структура INTF_ENTRY (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543559"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="54190-103">\_Структура записи intf</span><span class="sxs-lookup"><span data-stu-id="54190-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="54190-104">\[**Intf \_ ЗАПИСЬ** больше не поддерживается в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="54190-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="54190-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="54190-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="54190-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="54190-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="54190-107">Содержит подробные сведения о интерфейсе, который требуется клиенту RPC.</span><span class="sxs-lookup"><span data-stu-id="54190-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="54190-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54190-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="54190-109">Члены</span><span class="sxs-lookup"><span data-stu-id="54190-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="54190-110">**всзгуид**</span><span class="sxs-lookup"><span data-stu-id="54190-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="54190-111">Указатель на идентификатор GUID интерфейса, представленный в виде строки в Юникоде в следующем формате: "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="54190-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="54190-112">**всздескр**</span><span class="sxs-lookup"><span data-stu-id="54190-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="54190-113">Указатель на строку, содержащую описание интерфейса, которое извлекается службой настройки беспроводной связи (ВЗКСВК).</span><span class="sxs-lookup"><span data-stu-id="54190-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="54190-114">**двконтекст**</span><span class="sxs-lookup"><span data-stu-id="54190-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="54190-115">Зарезервировано для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="54190-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="54190-116">**улмедиастате**</span><span class="sxs-lookup"><span data-stu-id="54190-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="54190-117">Текущее состояние подключения носителя NDIS для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="54190-118">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="54190-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="54190-119">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="54190-120">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="54190-121"><dt> **\_ Состояние носителя \_ подключено**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="54190-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="54190-122">Носитель подключен.</span><span class="sxs-lookup"><span data-stu-id="54190-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="54190-123"><dt>**Носитель \_ СОСТОЯНИЕ " \_ отключено**</dt> <dt>0</dt> "</span><span class="sxs-lookup"><span data-stu-id="54190-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="54190-124">Носитель отключен.</span><span class="sxs-lookup"><span data-stu-id="54190-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="54190-125"><dt>**Носитель \_ \_Неизвестное состояние**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="54190-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="54190-126">Состояние носителя неизвестно.</span><span class="sxs-lookup"><span data-stu-id="54190-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54190-127">**улмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="54190-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="54190-128">Типы носителей NDIS, используемые в настоящее время сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="54190-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="54190-129">При запросе значение этого элемента равно **NdisMedium802 \_ 3** , как определено в файле заголовка *ндиспнп. h* .</span><span class="sxs-lookup"><span data-stu-id="54190-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="54190-130">**улфисикалмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="54190-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="54190-131">Тип носителя NDIS для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="54190-132">При запросе значение этого элемента равно **ндисфисикалмедиумвирелесслан** , как определено в файле заголовка *ндиспнп. h* .</span><span class="sxs-lookup"><span data-stu-id="54190-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="54190-133">**нинфрамоде**</span><span class="sxs-lookup"><span data-stu-id="54190-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="54190-134">Текущий режим инфраструктуры 802,11, установленный для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="54190-135">**наусмоде**</span><span class="sxs-lookup"><span data-stu-id="54190-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="54190-136">Текущий режим проверки подлинности 802,11, установленный для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="54190-137">В следующей таблице приведены возможные значения параметра, основанного на перечислении **\_ \_ \_ \_ режима аутентификации NDIS 802 11** , определенного в файле заголовка *нтддндис. h* .</span><span class="sxs-lookup"><span data-stu-id="54190-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="54190-138">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="54190-139">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="54190-140"><dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="54190-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="54190-141">Аутентификация IEEE 802,11 Open System.</span><span class="sxs-lookup"><span data-stu-id="54190-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="54190-142"><dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="54190-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="54190-143">Общая проверка подлинности IEEE 802,11, использующая ключ WEP.</span><span class="sxs-lookup"><span data-stu-id="54190-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="54190-144"><dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="54190-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="54190-145">Режим автоматического переключения.</span><span class="sxs-lookup"><span data-stu-id="54190-145">Auto-switch mode.</span></span> <span data-ttu-id="54190-146">При использовании режима автоматического переключения адаптер беспроводной сети (NIC) сначала пытается использовать режим общей проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="54190-147">В случае сбоя общего режима сетевая карта пытается использовать режим открытой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="54190-148"><dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="54190-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="54190-149">Безопасность защиты доступа к сети (WPA).</span><span class="sxs-lookup"><span data-stu-id="54190-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="54190-150">Проверка подлинности выполняется между запрашивающим стороной, средством проверки подлинности и сервером аутентификации через IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="54190-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="54190-151">Ключи шифрования являются динамическими и являются производными от процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="54190-152"><dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="54190-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="54190-153">Безопасность WPA с использованием общего ключа.</span><span class="sxs-lookup"><span data-stu-id="54190-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="54190-154">Проверка подлинности выполняется между запрашивающей стороной и проверкой подлинности по стандарту IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="54190-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="54190-155">Ключи шифрования являются динамическими и являются производными с помощью предварительно общего ключа, используемого запрашивающей стороной и средством проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="54190-156"><dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="54190-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="54190-157">Безопасность WPA.</span><span class="sxs-lookup"><span data-stu-id="54190-157">WPA security.</span></span> <span data-ttu-id="54190-158">Проверка подлинности выполняется с помощью предварительного ключа без проверки подлинности IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="54190-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="54190-159">Ключи шифрования являются статическими и являются производными через общий ключ.</span><span class="sxs-lookup"><span data-stu-id="54190-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="54190-160">Этот режим применим только к типам сетей ad hoc.</span><span class="sxs-lookup"><span data-stu-id="54190-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="54190-161"><dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="54190-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="54190-162">Безопасность WPA2.</span><span class="sxs-lookup"><span data-stu-id="54190-162">WPA2 security.</span></span> <span data-ttu-id="54190-163">Проверка подлинности выполняется между запрашивающим стороной, средством проверки подлинности и сервером аутентификации через IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="54190-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="54190-164">Ключи шифрования являются динамическими и являются производными от процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="54190-165"><dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="54190-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="54190-166">Указывает безопасность WPA2.</span><span class="sxs-lookup"><span data-stu-id="54190-166">Specifies WPA2 security.</span></span> <span data-ttu-id="54190-167">Проверка подлинности выполняется между запрашивающей стороной и проверкой подлинности через IEEE 802 1X.</span><span class="sxs-lookup"><span data-stu-id="54190-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="54190-168">Ключи шифрования являются динамическими и являются производными с помощью предварительно общего ключа, используемого запрашивающей стороной и средством проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="54190-169"><dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="54190-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="54190-170">Максимально возможное значение перечисления **\_ \_ \_ \_ режима проверки подлинности NDIS 802 11** .</span><span class="sxs-lookup"><span data-stu-id="54190-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="54190-171">Это недопустимое значение для режима проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54190-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="54190-172">**нвепстатус**</span><span class="sxs-lookup"><span data-stu-id="54190-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="54190-173">Текущий режим шифрования 802,11, установленный для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="54190-174">**двктлфлагс**</span><span class="sxs-lookup"><span data-stu-id="54190-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="54190-175">Битовая маска управляющего флага, указывающая, как ВЗКСВК работает в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="54190-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="54190-176">В следующей таблице приведены возможные значения битов.</span><span class="sxs-lookup"><span data-stu-id="54190-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="54190-177">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="54190-178">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="54190-179"><dt>**Интфктл \_ 0x0007 \_ маски cm**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="54190-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="54190-180">Битовая маска для режима сетевого фильтра.</span><span class="sxs-lookup"><span data-stu-id="54190-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="54190-181">ИНТФКТЛ \_ cm \_ Mask & двктлфлагс в результате имеет значение типа " \_ \_ сетевая инфраструктура NDIS 802 11" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="54190-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="54190-182">Полученное значение указывает, подключается ли ВЗКСВК к сетям инфраструктуры, сетям прямого подключения или к обоим типам сетей.</span><span class="sxs-lookup"><span data-stu-id="54190-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="54190-183"><dt>**Интфктл \_ ВКЛЮЧЕНО**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="54190-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="54190-184">Указывает, должен ли ВЗКСВК настраивать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="54190-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="54190-185"><dt>**Интфктл \_ РЕЗЕРВный**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="54190-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="54190-186">Если Предпочитаемая сеть недоступна, это значение указывает, должна ли ВЗКСВК автоматически настраивать сетевой адаптер для связи с любой доступной сетью.</span><span class="sxs-lookup"><span data-stu-id="54190-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="54190-187"><dt> **Интфктл \_ оидссупп**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="54190-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="54190-188">Указывает, поддерживает ли драйвер NIC все 802,11 OID, необходимые для работы ВЗКСВК.</span><span class="sxs-lookup"><span data-stu-id="54190-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="54190-189"><dt> **Интфктл \_ volatile**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="54190-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="54190-190">Указывает, должны ли параметры службы для этого интерфейса храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="54190-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="54190-191">Если это значение задано, эти параметры являются временными и не должны храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="54190-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="54190-192"><dt>0x0800</dt> <dt> **\_ Политика интфктл**</dt></span><span class="sxs-lookup"><span data-stu-id="54190-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="54190-193">Указывает, передаются ли параметры службы для этого интерфейса групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="54190-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="54190-194">Если это значение задано, параметры службы помещаются на локальный компьютер с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="54190-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="54190-195"><dt>**Интфктл \_ 8021XSUPP**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="54190-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="54190-196">Указывает, включена ли поддержка 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="54190-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="54190-197">**двдинфлагс**</span><span class="sxs-lookup"><span data-stu-id="54190-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="54190-198">Битовая маска динамических флагов, управляющих динамическим (непостоянным и нестатическим) поведением интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="54190-199">Эти биты полезны для активации динамических, временных изменений в способе, которым ВЗКСВК работает в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="54190-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="54190-200">Ни один из этих битов не сохраняется в реестре, поэтому параметры не сохранятся при перезапуске системы или отключении устройства и включении последовательности.</span><span class="sxs-lookup"><span data-stu-id="54190-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="54190-201">В следующей таблице приведены возможные значения битов.</span><span class="sxs-lookup"><span data-stu-id="54190-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="54190-202">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="54190-203">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="54190-204"><dt>**Интфдин \_ Несканирование**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="54190-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="54190-205">Указывает, что ВЗКСВК не должен запрашивать у интерфейса активную проверку, а вместо этого использовать кэшированные значения в драйвере сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="54190-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54190-206">**двкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="54190-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="54190-207">Указывает возможности драйвера.</span><span class="sxs-lookup"><span data-stu-id="54190-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="54190-208">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="54190-209">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="54190-210"><dt>**Интфкап \_ 0x000000ff \_ максимальной \_ маски шифра**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="54190-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="54190-211">Младшие биты этого элемента используются для указания максимального поддерживаемого шифрования.</span><span class="sxs-lookup"><span data-stu-id="54190-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="54190-212">Возможные значения — это некоторые значения перечисления, определенные в структуре **\_ \_ \_ \_ состояния WEP 802 11** в файле заголовка *нтддндис. h* , который содержится в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="54190-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="54190-213">Значение Ndis802 \_ 11Encryption1Enabled (2) указывает, что поддерживается WEP.</span><span class="sxs-lookup"><span data-stu-id="54190-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="54190-214">TKIP и AES не поддерживаются, а ключ передачи может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="54190-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="54190-215">Значение Ndis802 \_ 11Encryption2Enabled (9) указывает, что поддерживаются протоколы TKIP и WEP.</span><span class="sxs-lookup"><span data-stu-id="54190-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="54190-216">Алгоритм AES не поддерживается, и доступен ключ передачи.</span><span class="sxs-lookup"><span data-stu-id="54190-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="54190-217">Значение Ndis802 \_ 11Encryption3Enabled (11) указывает, что поддерживаются AES, TKIP и WEP, а также доступен ключ передачи.</span><span class="sxs-lookup"><span data-stu-id="54190-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="54190-218">Ndis802 \_ 11EncryptionNotSupported (8) указывает, что WEP-ключ не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="54190-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="54190-219"><dt>**Интфкап \_**</dt> <dt>0x00000100</dt> SSN</span><span class="sxs-lookup"><span data-stu-id="54190-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="54190-220">Указывает поддержку для простой безопасной сети (SSN), которая является подмножеством стандарта 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="54190-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="54190-221">SSN периодически изменяет ключ шифрования, в отличие от стандарта WEP (Wired Equivalent Privacy), который использует статический ключ.</span><span class="sxs-lookup"><span data-stu-id="54190-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="54190-222">Чтобы использовать SSN, максимальный поддерживаемый шифр должен быть не менее TKIP.</span><span class="sxs-lookup"><span data-stu-id="54190-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="54190-223">SSN был разработан консорциумом по поставщикам 2002 в качестве промежуточного подхода к повышению безопасности беспроводных локальных сетей во время выполнения стандарта IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="54190-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="54190-224"><dt>**Интфкап \_ 80211I**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="54190-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="54190-225">Обозначает поддержку стандарта IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="54190-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="54190-226">**рдниккапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="54190-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="54190-227">Набор возможностей для 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="54190-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="54190-228">Функция [**взккуеринтерфаце**](wzcqueryinterface.md) возвращает данные **рдниккапабилитиес** при вызове с флагом **intf \_ CAPABILITIES** , переданным в параметр *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="54190-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="54190-229">Если вызов функции выполнен успешно, элемент **pData** в структуре **необработанных \_ данных** содержит структуру **возможностей intf \_ 80211 \_** .</span><span class="sxs-lookup"><span data-stu-id="54190-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="54190-230">**рдссид**</span><span class="sxs-lookup"><span data-stu-id="54190-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="54190-231">Двоичные данные, содержащие SSID 802,11, которые в настоящее время настроены для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="54190-232">Функция [**взккуеринтерфаце**](wzcqueryinterface.md) возвращает данные **рдссид** при вызове с флагом **\_ SSID intf** , переданным в параметр *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="54190-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="54190-233">Если вызов функции выполнен успешно, элемент **двдатален** структуры **необработанных \_ данных** содержит элемент **ссидленгс** структуры **\_ \_ \_ SSID NDIS 802 11** , а элемент **pData** структуры **необработанных \_ данных** содержит элемент **SSID** в структуре **NDIS \_ 802 \_ 11 \_** .</span><span class="sxs-lookup"><span data-stu-id="54190-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="54190-234">Структура **\_ \_ \_ SSID NDIS 802 11** определена в файле заголовка *нтддндис. h* .</span><span class="sxs-lookup"><span data-stu-id="54190-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="54190-235">**рдбссид**</span><span class="sxs-lookup"><span data-stu-id="54190-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="54190-236">Двоичные данные, содержащие параметр BSSID 802,11, настроенный в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="54190-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="54190-237">Функция [**взккуеринтерфаце**](wzcqueryinterface.md) возвращает данные **рдбссид** при вызове с флагом **\_ BSSID intf** , переданным в параметр *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="54190-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="54190-238">Если вызов функции выполнен успешно, элемент **двдатален** структуры **необработанных \_ данных** содержит размер структуры **\_ \_ \_ Mac- \_ адреса (NDIS 802 11** ), а элемент **PData** в структуре **необработанных \_ данных** содержит структуру **\_ \_ \_ Mac- \_ адреса NDIS 802 11** .</span><span class="sxs-lookup"><span data-stu-id="54190-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="54190-239">Структура **\_ \_ \_ Mac- \_ адреса в NDIS 802 11** определена в файле заголовка *нтддндис. h* .</span><span class="sxs-lookup"><span data-stu-id="54190-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="54190-240">**рдбссидлист**</span><span class="sxs-lookup"><span data-stu-id="54190-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="54190-241">Двоичные данные, содержащие список Бссидс, которые были в последний раз извлечены ВЗКСВК.</span><span class="sxs-lookup"><span data-stu-id="54190-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="54190-242">Функция [**взккуеринтерфаце**](wzcqueryinterface.md) возвращает данные **рдбссидлист** при вызове с флагом **intf \_ бссидлист** , переданным в параметре *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="54190-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="54190-243">Если вызов функции выполнен успешно, элемент **двдатален** структуры **необработанных \_ данных** содержит длину буфера с возвращаемыми данными, а элемент **pData** в структуре **необработанных \_ данных** содержит структуру **\_ \_ \_ \_ списка конфигурации ВЗК 802 11** .</span><span class="sxs-lookup"><span data-stu-id="54190-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="54190-244">**рдстссидлист**</span><span class="sxs-lookup"><span data-stu-id="54190-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="54190-245">Двоичные данные, содержащие список предпочитаемых сетей, настроенных для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="54190-246">Функция [**взккуеринтерфаце**](wzcqueryinterface.md) возвращает данные **рдстссидлист** при вызове с флагом **intf \_ префлист** , переданным в параметре *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="54190-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="54190-247">Если вызов функции выполнен успешно, элемент **двдатален** структуры **необработанных \_ данных** содержит длину буфера с возвращаемыми данными, а элемент **pData** в структуре **необработанных \_ данных** содержит структуру **\_ \_ \_ \_ списка конфигурации ВЗК 802 11** .</span><span class="sxs-lookup"><span data-stu-id="54190-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="54190-248">Если в настоящее время подключена одна из предпочитаемых сетей, то в качестве члена **двктлфлагс** в структуре **\_ \_ конфигурации WLAN ВЗК** для сети будет установлен бит **взкктл \_ Media \_ Connected** (0x0400).</span><span class="sxs-lookup"><span data-stu-id="54190-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="54190-249">**рдктрлдата**</span><span class="sxs-lookup"><span data-stu-id="54190-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="54190-250">Двоичные данные, используемые с другими флагами управления, при установке дополнительных параметров интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54190-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54190-251">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54190-251">Remarks</span></span>

<span data-ttu-id="54190-252">Структура **\_ записи intf** используется функциями [**взккуеринтерфаце**](wzcqueryinterface.md) и [**взкрефрешинтерфаце**](wzcrefreshinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="54190-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="54190-253">Структура **необработанных \_ данных** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="54190-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="54190-254">Элемент *pData* указывает на двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="54190-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="54190-255">*Двдатален* указывает число байтов, на которые указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="54190-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="54190-256">Файл заголовка *взксапи. h* недоступен в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="54190-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54190-257">Требования</span><span class="sxs-lookup"><span data-stu-id="54190-257">Requirements</span></span>



| <span data-ttu-id="54190-258">Требование</span><span class="sxs-lookup"><span data-stu-id="54190-258">Requirement</span></span> | <span data-ttu-id="54190-259">Значение</span><span class="sxs-lookup"><span data-stu-id="54190-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54190-260">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54190-260">Minimum supported client</span></span><br/> | <span data-ttu-id="54190-261">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="54190-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54190-262">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54190-262">Minimum supported server</span></span><br/> | <span data-ttu-id="54190-263">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54190-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54190-264">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="54190-264">End of client support</span></span><br/>    | <span data-ttu-id="54190-265">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="54190-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="54190-266">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="54190-266">End of server support</span></span><br/>    | <span data-ttu-id="54190-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="54190-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="54190-268">Header</span><span class="sxs-lookup"><span data-stu-id="54190-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="54190-269"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="54190-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54190-270">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54190-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54190-271">**взценуминтерфацес**</span><span class="sxs-lookup"><span data-stu-id="54190-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="54190-272">**взккуеринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="54190-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="54190-273">**взкрефрешинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="54190-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




