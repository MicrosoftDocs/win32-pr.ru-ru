---
title: Класс MDM_Policy_Config01_WirelessDisplay02
description: '\_Класс политики MDM \_ Config01 \_ WirelessDisplay02 представляет доступные политики беспроводного просмотра.'
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- Класс MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b99183f8fdf599df8b5c1b4e82b9b536f47019
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988719"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a><span data-ttu-id="57773-105">\_Класс политики MDM \_ Config01 \_ WirelessDisplay02</span><span class="sxs-lookup"><span data-stu-id="57773-105">MDM\_Policy\_Config01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="57773-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="57773-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="57773-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="57773-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="57773-108">Класс **\_ политики MDM \_ Config01 \_ WirelessDisplay02** представляет доступные политики беспроводного просмотра.</span><span class="sxs-lookup"><span data-stu-id="57773-108">The **MDM\_Policy\_Config01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="57773-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="57773-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57773-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57773-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
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

## <a name="members"></a><span data-ttu-id="57773-111">Члены</span><span class="sxs-lookup"><span data-stu-id="57773-111">Members</span></span>

<span data-ttu-id="57773-112">Класс **\_ политики MDM \_ Config01 \_ WirelessDisplay02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="57773-112">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="57773-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="57773-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57773-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="57773-114">Properties</span></span>

<span data-ttu-id="57773-115">Класс **\_ политики MDM \_ Config01 \_ WirelessDisplay02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="57773-115">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="57773-116">алловмднсадвертисемент</span><span class="sxs-lookup"><span data-stu-id="57773-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="57773-119">алловмднсдисковери</span><span class="sxs-lookup"><span data-stu-id="57773-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="57773-122">алловпрожектионфромпк</span><span class="sxs-lookup"><span data-stu-id="57773-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="57773-125">алловпрожектионфромпковеринфраструктуре</span><span class="sxs-lookup"><span data-stu-id="57773-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="57773-128">алловпрожектионтопк</span><span class="sxs-lookup"><span data-stu-id="57773-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="57773-131">алловпрожектионтопковеринфраструктуре</span><span class="sxs-lookup"><span data-stu-id="57773-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="57773-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="57773-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57773-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="57773-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="57773-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57773-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57773-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57773-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="57773-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="57773-141">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="57773-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="57773-142">Для этого класса строка имеет значение "Вирелессдисплай".</span><span class="sxs-lookup"><span data-stu-id="57773-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="57773-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="57773-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="57773-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57773-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57773-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57773-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="57773-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="57773-147">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="57773-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="57773-148">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="57773-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="57773-149">рекуирепинфорпаиринг</span><span class="sxs-lookup"><span data-stu-id="57773-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="57773-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="57773-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="57773-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="57773-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57773-152">Требования</span><span class="sxs-lookup"><span data-stu-id="57773-152">Requirements</span></span>



| <span data-ttu-id="57773-153">Требование</span><span class="sxs-lookup"><span data-stu-id="57773-153">Requirement</span></span> | <span data-ttu-id="57773-154">Значение</span><span class="sxs-lookup"><span data-stu-id="57773-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57773-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57773-155">Minimum supported client</span></span><br/> | <span data-ttu-id="57773-156">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="57773-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="57773-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57773-157">Minimum supported server</span></span><br/> | <span data-ttu-id="57773-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="57773-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="57773-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="57773-159">Namespace</span></span><br/>                | <span data-ttu-id="57773-160">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="57773-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="57773-161">MOF</span><span class="sxs-lookup"><span data-stu-id="57773-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57773-162"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57773-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="57773-163">DLL</span><span class="sxs-lookup"><span data-stu-id="57773-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57773-164"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57773-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

