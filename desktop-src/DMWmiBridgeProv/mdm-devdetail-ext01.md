---
title: Класс MDM_DevDetail_Ext01
description: Класс MDM \_ DevDetail \_ Ext01 обрабатывает объект управления, который предоставляет параметры конкретного устройства для сервера OMA DM.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- Класс MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803125"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="24370-105">\_Класс MDM DevDetail \_ Ext01</span><span class="sxs-lookup"><span data-stu-id="24370-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="24370-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="24370-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="24370-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="24370-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="24370-108">Класс **MDM \_ DevDetail \_ Ext01** обрабатывает объект управления, который предоставляет параметры конкретного устройства для сервера OMA DM.</span><span class="sxs-lookup"><span data-stu-id="24370-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="24370-109">Эти параметры устройства не отправляются с клиента на сервер автоматически, но их можно запрашивать с помощью команд OMA DM.</span><span class="sxs-lookup"><span data-stu-id="24370-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="24370-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="24370-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="24370-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24370-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="24370-112">Члены</span><span class="sxs-lookup"><span data-stu-id="24370-112">Members</span></span>

<span data-ttu-id="24370-113">Класс **MDM \_ DevDetail \_ Ext01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24370-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="24370-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="24370-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24370-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="24370-115">Properties</span></span>

<span data-ttu-id="24370-116">Класс **MDM \_ DevDetail \_ Ext01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="24370-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="24370-117">девицехардваредата</span><span class="sxs-lookup"><span data-stu-id="24370-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24370-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24370-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24370-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="24370-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="24370-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="24370-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24370-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24370-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24370-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24370-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24370-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24370-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24370-124">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="24370-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="24370-125">Для этого класса строка имеет значение "ext"</span><span class="sxs-lookup"><span data-stu-id="24370-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="24370-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="24370-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24370-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24370-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24370-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24370-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24370-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24370-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24370-130">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="24370-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="24370-131">Для этого класса строка имеет значение "./Девдетаил/"</span><span class="sxs-lookup"><span data-stu-id="24370-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="24370-132">вланмакаддресс</span><span class="sxs-lookup"><span data-stu-id="24370-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24370-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24370-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24370-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="24370-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24370-135">Требования</span><span class="sxs-lookup"><span data-stu-id="24370-135">Requirements</span></span>



| <span data-ttu-id="24370-136">Требование</span><span class="sxs-lookup"><span data-stu-id="24370-136">Requirement</span></span> | <span data-ttu-id="24370-137">Значение</span><span class="sxs-lookup"><span data-stu-id="24370-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24370-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24370-138">Minimum supported client</span></span><br/> | <span data-ttu-id="24370-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="24370-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24370-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24370-140">Minimum supported server</span></span><br/> | <span data-ttu-id="24370-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="24370-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="24370-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24370-142">Namespace</span></span><br/>                | <span data-ttu-id="24370-143">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="24370-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="24370-144">MOF</span><span class="sxs-lookup"><span data-stu-id="24370-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24370-145"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24370-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="24370-146">DLL</span><span class="sxs-lookup"><span data-stu-id="24370-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24370-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24370-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24370-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24370-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24370-149">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="24370-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

