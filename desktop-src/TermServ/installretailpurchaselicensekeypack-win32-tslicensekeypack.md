---
title: Метод Инсталлретаилпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по розничному каналу.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инсталлретаилпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Инсталлретаилпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Инсталлретаилпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672538"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="30a11-106">Метод Инсталлретаилпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="30a11-106">InstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="30a11-107">Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по розничному каналу.</span><span class="sxs-lookup"><span data-stu-id="30a11-107">Installs a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a11-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30a11-108">Syntax</span></span>


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="30a11-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="30a11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a11-110">*слиценсекоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="30a11-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a11-111">Содержит 25-символьный код лицензии.</span><span class="sxs-lookup"><span data-stu-id="30a11-111">Contains the 25-character license code.</span></span> <span data-ttu-id="30a11-112">В качестве входных данных должно быть задано только 25-символьная строка символов.</span><span class="sxs-lookup"><span data-stu-id="30a11-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="30a11-113">Переносы не добавляются.</span><span class="sxs-lookup"><span data-stu-id="30a11-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="30a11-114">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="30a11-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a11-115">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="30a11-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a11-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30a11-116">Return value</span></span>

<span data-ttu-id="30a11-117">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="30a11-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="30a11-118">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="30a11-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="30a11-119">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="30a11-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30a11-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30a11-120">Remarks</span></span>

<span data-ttu-id="30a11-121">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="30a11-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="30a11-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="30a11-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30a11-123">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="30a11-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30a11-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="30a11-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30a11-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="30a11-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="30a11-126">Требования</span><span class="sxs-lookup"><span data-stu-id="30a11-126">Requirements</span></span>



| <span data-ttu-id="30a11-127">Требование</span><span class="sxs-lookup"><span data-stu-id="30a11-127">Requirement</span></span> | <span data-ttu-id="30a11-128">Значение</span><span class="sxs-lookup"><span data-stu-id="30a11-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a11-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30a11-129">Minimum supported client</span></span><br/> | <span data-ttu-id="30a11-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30a11-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="30a11-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30a11-131">Minimum supported server</span></span><br/> | <span data-ttu-id="30a11-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30a11-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="30a11-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="30a11-133">Namespace</span></span><br/>                | <span data-ttu-id="30a11-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="30a11-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="30a11-135">MOF</span><span class="sxs-lookup"><span data-stu-id="30a11-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30a11-136"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30a11-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="30a11-137">DLL</span><span class="sxs-lookup"><span data-stu-id="30a11-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30a11-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30a11-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a11-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30a11-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a11-140">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="30a11-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

