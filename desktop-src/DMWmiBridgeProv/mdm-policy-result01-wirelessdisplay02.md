---
title: Класс MDM_Policy_Result01_WirelessDisplay02
description: '\_Класс политики MDM \_ Result01 \_ WirelessDisplay02 представляет доступные политики беспроводного просмотра.'
ms.assetid: fbdfa785-8747-47b4-9802-da1c245ca222
keywords:
- Класс MDM_Policy_Result01_WirelessDisplay02
- MDM_Policy_Result01_WirelessDisplay02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WirelessDisplay02
- MDM_Policy_Result01_WirelessDisplay02.InstanceID
- MDM_Policy_Result01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f4e309d1c54f12d99dfbeaa0b80807249e61fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071165"
---
# <a name="mdm_policy_result01_wirelessdisplay02-class"></a><span data-ttu-id="9878e-105">\_Класс политики MDM \_ Result01 \_ WirelessDisplay02</span><span class="sxs-lookup"><span data-stu-id="9878e-105">MDM\_Policy\_Result01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="9878e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9878e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9878e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9878e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9878e-108">Класс **\_ политики MDM \_ Result01 \_ WirelessDisplay02** представляет доступные политики беспроводного просмотра.</span><span class="sxs-lookup"><span data-stu-id="9878e-108">The **MDM\_Policy\_Result01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="9878e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9878e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9878e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9878e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="9878e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9878e-111">Members</span></span>

<span data-ttu-id="9878e-112">Класс **\_ политики MDM \_ Result01 \_ WirelessDisplay02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9878e-112">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="9878e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9878e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9878e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9878e-114">Properties</span></span>

<span data-ttu-id="9878e-115">Класс **\_ политики MDM \_ Result01 \_ WirelessDisplay02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9878e-115">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9878e-116">алловмднсадвертисемент</span><span class="sxs-lookup"><span data-stu-id="9878e-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9878e-119">алловмднсдисковери</span><span class="sxs-lookup"><span data-stu-id="9878e-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9878e-122">алловпрожектионфромпк</span><span class="sxs-lookup"><span data-stu-id="9878e-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9878e-125">алловпрожектионфромпковеринфраструктуре</span><span class="sxs-lookup"><span data-stu-id="9878e-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9878e-128">алловпрожектионтопк</span><span class="sxs-lookup"><span data-stu-id="9878e-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9878e-131">алловпрожектионтопковеринфраструктуре</span><span class="sxs-lookup"><span data-stu-id="9878e-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9878e-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="9878e-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9878e-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9878e-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9878e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9878e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9878e-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9878e-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9878e-141">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="9878e-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="9878e-142">Для этого класса строка имеет значение "Вирелессдисплай".</span><span class="sxs-lookup"><span data-stu-id="9878e-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="9878e-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9878e-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9878e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9878e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9878e-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9878e-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9878e-147">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="9878e-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="9878e-148">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="9878e-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="9878e-149">рекуирепинфорпаиринг</span><span class="sxs-lookup"><span data-stu-id="9878e-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9878e-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9878e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9878e-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9878e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9878e-152">Требования</span><span class="sxs-lookup"><span data-stu-id="9878e-152">Requirements</span></span>



| <span data-ttu-id="9878e-153">Требование</span><span class="sxs-lookup"><span data-stu-id="9878e-153">Requirement</span></span> | <span data-ttu-id="9878e-154">Значение</span><span class="sxs-lookup"><span data-stu-id="9878e-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9878e-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9878e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="9878e-156">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9878e-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9878e-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9878e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="9878e-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9878e-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="9878e-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9878e-159">Namespace</span></span><br/>                | <span data-ttu-id="9878e-160">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9878e-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="9878e-161">MOF</span><span class="sxs-lookup"><span data-stu-id="9878e-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9878e-162"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9878e-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="9878e-163">DLL</span><span class="sxs-lookup"><span data-stu-id="9878e-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9878e-164"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9878e-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

