---
title: Класс MDM_VPNv2_CryptographySuite03
description: Класс MDM \_ Поддержка vpnv2 \_ CryptographySuite03 содержит сведения о шифровании для собственного профиля VPN.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- Класс MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490662"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="f4329-105">\_Класс MDM поддержка vpnv2 \_ CryptographySuite03</span><span class="sxs-lookup"><span data-stu-id="f4329-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="f4329-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f4329-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f4329-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f4329-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f4329-108">Класс **MDM \_ Поддержка vpnv2 \_ CryptographySuite03** содержит сведения о шифровании для собственного профиля VPN.</span><span class="sxs-lookup"><span data-stu-id="f4329-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="f4329-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f4329-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4329-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4329-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="f4329-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f4329-111">Members</span></span>

<span data-ttu-id="f4329-112">Класс **MDM \_ Поддержка vpnv2 \_ CryptographySuite03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f4329-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="f4329-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4329-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4329-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4329-114">Properties</span></span>

<span data-ttu-id="f4329-115">Класс **MDM \_ Поддержка vpnv2 \_ CryptographySuite03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f4329-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f4329-116">аусентикатионтрансформконстантс</span><span class="sxs-lookup"><span data-stu-id="f4329-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4329-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4329-119">Цифертрансформконстантс</span><span class="sxs-lookup"><span data-stu-id="f4329-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4329-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4329-122">DHGroup</span><span class="sxs-lookup"><span data-stu-id="f4329-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4329-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4329-125">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="f4329-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4329-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4329-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f4329-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4329-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4329-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4329-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4329-132">Узел, содержащий свойства туннелей IPSec.</span><span class="sxs-lookup"><span data-stu-id="f4329-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="f4329-133">интегритичеккмесод</span><span class="sxs-lookup"><span data-stu-id="f4329-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4329-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4329-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f4329-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4329-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4329-139">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4329-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4329-140">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f4329-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="f4329-141">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/нативепрофиле"</span><span class="sxs-lookup"><span data-stu-id="f4329-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="f4329-142">пфсграуп</span><span class="sxs-lookup"><span data-stu-id="f4329-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4329-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4329-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4329-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4329-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4329-145">Требования</span><span class="sxs-lookup"><span data-stu-id="f4329-145">Requirements</span></span>



| <span data-ttu-id="f4329-146">Требование</span><span class="sxs-lookup"><span data-stu-id="f4329-146">Requirement</span></span> | <span data-ttu-id="f4329-147">Значение</span><span class="sxs-lookup"><span data-stu-id="f4329-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4329-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4329-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f4329-149">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f4329-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4329-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4329-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f4329-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4329-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f4329-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4329-152">Namespace</span></span><br/>                | <span data-ttu-id="f4329-153">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f4329-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f4329-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f4329-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4329-155"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4329-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4329-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f4329-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4329-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4329-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

