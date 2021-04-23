---
title: Класс MDM_DevDetail
description: Класс MDM \_ DevDetail обрабатывает объект управления, который предоставляет параметры, относящиеся к устройству, к серверу OMA DM.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- Класс MDM_DevDetail
- MDM_DevDetail класс, описание
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654597"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="e9b5e-105">\_Класс MDM DevDetail</span><span class="sxs-lookup"><span data-stu-id="e9b5e-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="e9b5e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e9b5e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e9b5e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e9b5e-108">Класс **MDM \_ DevDetail** обрабатывает объект управления, который предоставляет параметры, относящиеся к устройству, к серверу OMA DM.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="e9b5e-109">Эти параметры устройства не отправляются с клиента на сервер автоматически, но их можно запрашивать с помощью команд OMA DM.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="e9b5e-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b5e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9b5e-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="e9b5e-112">Члены</span><span class="sxs-lookup"><span data-stu-id="e9b5e-112">Members</span></span>

<span data-ttu-id="e9b5e-113">Класс **MDM \_ DevDetail** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e9b5e-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="e9b5e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9b5e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9b5e-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9b5e-115">Properties</span></span>

<span data-ttu-id="e9b5e-116">Класс **MDM \_ DevDetail** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e9b5e-117">девтип</span><span class="sxs-lookup"><span data-stu-id="e9b5e-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9b5e-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e9b5e-120">фвв</span><span class="sxs-lookup"><span data-stu-id="e9b5e-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9b5e-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e9b5e-123">хвв</span><span class="sxs-lookup"><span data-stu-id="e9b5e-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9b5e-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9b5e-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9b5e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9b5e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9b5e-130">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="e9b5e-131">Для этого класса строка имеет значение "DevDetail".</span><span class="sxs-lookup"><span data-stu-id="e9b5e-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="e9b5e-132">лргобж</span><span class="sxs-lookup"><span data-stu-id="e9b5e-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9b5e-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e9b5e-135">ПВТ</span><span class="sxs-lookup"><span data-stu-id="e9b5e-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9b5e-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9b5e-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9b5e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-141">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9b5e-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9b5e-142">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="e9b5e-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="e9b5e-143">SwV</span><span class="sxs-lookup"><span data-stu-id="e9b5e-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9b5e-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9b5e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9b5e-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9b5e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9b5e-146">Требования</span><span class="sxs-lookup"><span data-stu-id="e9b5e-146">Requirements</span></span>



| <span data-ttu-id="e9b5e-147">Требование</span><span class="sxs-lookup"><span data-stu-id="e9b5e-147">Requirement</span></span> | <span data-ttu-id="e9b5e-148">Значение</span><span class="sxs-lookup"><span data-stu-id="e9b5e-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b5e-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9b5e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b5e-150">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e9b5e-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9b5e-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9b5e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b5e-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e9b5e-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e9b5e-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9b5e-153">Namespace</span></span><br/>                | <span data-ttu-id="e9b5e-154">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e9b5e-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e9b5e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="e9b5e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9b5e-156"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9b5e-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9b5e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e9b5e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9b5e-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9b5e-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b5e-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9b5e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b5e-160">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="e9b5e-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

