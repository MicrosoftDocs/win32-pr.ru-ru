---
title: Класс MDM_EnterpriseModernAppManagement_AppManagement01_02
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02 указывает, следует ли блокировать обновление определенного приложения с помощью автоматического обновления.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491952"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="f661e-105">\_Класс MDM ентерприсемодернаппманажемент \_ AppManagement01 \_ 02</span><span class="sxs-lookup"><span data-stu-id="f661e-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="f661e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f661e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f661e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f661e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f661e-108">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02** указывает, следует ли блокировать обновление определенного приложения с помощью автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="f661e-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="f661e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f661e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f661e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f661e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="f661e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f661e-111">Members</span></span>

<span data-ttu-id="f661e-112">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f661e-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="f661e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f661e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f661e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f661e-114">Properties</span></span>

<span data-ttu-id="f661e-115">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="f661e-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f661e-116">донотупдате</span><span class="sxs-lookup"><span data-stu-id="f661e-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f661e-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f661e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f661e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f661e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f661e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f661e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f661e-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f661e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f661e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f661e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f661e-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f661e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f661e-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f661e-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f661e-124">Для этого класса строка является экземпляром имени семейства пакетов.</span><span class="sxs-lookup"><span data-stu-id="f661e-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="f661e-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f661e-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f661e-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f661e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f661e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f661e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f661e-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f661e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f661e-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f661e-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="f661e-130">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/аппманажемент/*EnterpriseID*"</span><span class="sxs-lookup"><span data-stu-id="f661e-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f661e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f661e-131">Requirements</span></span>



| <span data-ttu-id="f661e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f661e-132">Requirement</span></span> | <span data-ttu-id="f661e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f661e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f661e-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f661e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f661e-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f661e-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f661e-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f661e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f661e-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f661e-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f661e-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f661e-138">Namespace</span></span><br/>                | <span data-ttu-id="f661e-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f661e-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f661e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f661e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f661e-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f661e-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f661e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f661e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f661e-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f661e-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f661e-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f661e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f661e-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="f661e-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

