---
title: Класс MDM_Policy_Result01_Authentication02
description: '\_Класс политики MDM \_ Result01 \_ Authentication02 представляет доступные политики управления аутентификацией.'
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- Класс MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d80979fe7b025ea7b0677436036c8760d4b0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137535"
---
# <a name="mdm_policy_result01_authentication02-class"></a><span data-ttu-id="c2cf0-105">\_Класс политики MDM \_ Result01 \_ Authentication02</span><span class="sxs-lookup"><span data-stu-id="c2cf0-105">MDM\_Policy\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="c2cf0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c2cf0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c2cf0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c2cf0-108">Класс **\_ политики MDM \_ Result01 \_ Authentication02** представляет доступные политики управления аутентификацией.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-108">The **MDM\_Policy\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="c2cf0-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cf0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2cf0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="c2cf0-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c2cf0-111">Members</span></span>

<span data-ttu-id="c2cf0-112">Класс **\_ политики MDM \_ Result01 \_ Authentication02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c2cf0-112">The **MDM\_Policy\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="c2cf0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2cf0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2cf0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2cf0-114">Properties</span></span>

<span data-ttu-id="c2cf0-115">Класс **\_ политики MDM \_ Result01 \_ Authentication02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-115">The **MDM\_Policy\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c2cf0-116">алловаадпассвордресет</span><span class="sxs-lookup"><span data-stu-id="c2cf0-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2cf0-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c2cf0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c2cf0-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="c2cf0-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2cf0-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c2cf0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c2cf0-122">алловфидодевицесигнон</span><span class="sxs-lookup"><span data-stu-id="c2cf0-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2cf0-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c2cf0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c2cf0-125">алловсекондаряусентикатиондевице</span><span class="sxs-lookup"><span data-stu-id="c2cf0-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2cf0-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c2cf0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2cf0-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2cf0-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2cf0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2cf0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2cf0-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="c2cf0-133">Для этого класса строка имеет значение Authentication.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="c2cf0-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2cf0-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c2cf0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2cf0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2cf0-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2cf0-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2cf0-138">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="c2cf0-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="c2cf0-139">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="c2cf0-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2cf0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="c2cf0-140">Requirements</span></span>



| <span data-ttu-id="c2cf0-141">Требование</span><span class="sxs-lookup"><span data-stu-id="c2cf0-141">Requirement</span></span> | <span data-ttu-id="c2cf0-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c2cf0-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cf0-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2cf0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cf0-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c2cf0-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2cf0-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2cf0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cf0-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c2cf0-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c2cf0-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2cf0-147">Namespace</span></span><br/>                | <span data-ttu-id="c2cf0-148">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c2cf0-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c2cf0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c2cf0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2cf0-150"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf0-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2cf0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c2cf0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2cf0-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf0-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cf0-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2cf0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cf0-154">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="c2cf0-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

