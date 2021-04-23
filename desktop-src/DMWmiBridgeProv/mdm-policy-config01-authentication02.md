---
title: Класс MDM_Policy_Config01_Authentication02
description: '\_Класс политики MDM \_ Config01 \_ Authentication02 представляет доступные политики управления аутентификацией.'
ms.assetid: 928e0b60-5533-45dc-90e6-be7d70210138
keywords:
- Класс MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02.InstanceID
- MDM_Policy_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfab66a548f4a92c445f748aca1bb15758ac48c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654457"
---
# <a name="mdm_policy_config01_authentication02-class"></a><span data-ttu-id="17386-105">\_Класс политики MDM \_ Config01 \_ Authentication02</span><span class="sxs-lookup"><span data-stu-id="17386-105">MDM\_Policy\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="17386-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="17386-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="17386-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="17386-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="17386-108">Класс **\_ политики MDM \_ Config01 \_ Authentication02** представляет доступные политики управления аутентификацией.</span><span class="sxs-lookup"><span data-stu-id="17386-108">The **MDM\_Policy\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="17386-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="17386-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17386-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17386-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="17386-111">Члены</span><span class="sxs-lookup"><span data-stu-id="17386-111">Members</span></span>

<span data-ttu-id="17386-112">Класс **\_ политики MDM \_ Config01 \_ Authentication02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="17386-112">The **MDM\_Policy\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="17386-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="17386-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17386-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="17386-114">Properties</span></span>

<span data-ttu-id="17386-115">Класс **\_ политики MDM \_ Config01 \_ Authentication02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="17386-115">The **MDM\_Policy\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="17386-116">алловаадпассвордресет</span><span class="sxs-lookup"><span data-stu-id="17386-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17386-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="17386-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17386-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="17386-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17386-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="17386-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17386-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="17386-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17386-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="17386-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17386-122">алловфидодевицесигнон</span><span class="sxs-lookup"><span data-stu-id="17386-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17386-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="17386-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17386-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="17386-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17386-125">алловсекондаряусентикатиондевице</span><span class="sxs-lookup"><span data-stu-id="17386-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17386-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="17386-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17386-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="17386-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17386-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="17386-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17386-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17386-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17386-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17386-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17386-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17386-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17386-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="17386-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="17386-133">Для этого класса строка имеет значение Authentication.</span><span class="sxs-lookup"><span data-stu-id="17386-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="17386-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="17386-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17386-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17386-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17386-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17386-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17386-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17386-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17386-138">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="17386-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="17386-139">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="17386-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17386-140">Требования</span><span class="sxs-lookup"><span data-stu-id="17386-140">Requirements</span></span>



| <span data-ttu-id="17386-141">Требование</span><span class="sxs-lookup"><span data-stu-id="17386-141">Requirement</span></span> | <span data-ttu-id="17386-142">Значение</span><span class="sxs-lookup"><span data-stu-id="17386-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17386-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17386-143">Minimum supported client</span></span><br/> | <span data-ttu-id="17386-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="17386-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17386-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17386-145">Minimum supported server</span></span><br/> | <span data-ttu-id="17386-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="17386-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="17386-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="17386-147">Namespace</span></span><br/>                | <span data-ttu-id="17386-148">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="17386-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="17386-149">MOF</span><span class="sxs-lookup"><span data-stu-id="17386-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17386-150"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17386-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="17386-151">DLL</span><span class="sxs-lookup"><span data-stu-id="17386-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17386-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17386-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17386-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17386-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17386-154">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="17386-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

