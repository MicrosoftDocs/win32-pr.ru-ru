---
title: Метод Унинсталллиценсекэйпакквисид класса Win32_TSLicenseKeyPack
description: Удаляет службы удаленных рабочих столов пакет лицензионных ключей с указанным идентификатором пакета ключей.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Унинсталллиценсекэйпакквисид
- Службы удаленных рабочих столов метода Унинсталллиценсекэйпакквисид, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Унинсталллиценсекэйпакквисид
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489363"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="3a5fc-106">Метод Унинсталллиценсекэйпакквисид \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="3a5fc-106">UninstallLicenseKeyPackWithId method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="3a5fc-107">Удаляет службы удаленных рабочих столов пакет лицензионных ключей с указанным идентификатором пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="3a5fc-107">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a5fc-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="3a5fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a5fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5fc-110">*Кэйпаккид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a5fc-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5fc-111">Идентификатор удаляемого пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="3a5fc-111">The identifier of the key pack to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5fc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a5fc-112">Return value</span></span>

<span data-ttu-id="3a5fc-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3a5fc-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3a5fc-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3a5fc-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3a5fc-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3a5fc-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5fc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3a5fc-116">Requirements</span></span>



| <span data-ttu-id="3a5fc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3a5fc-117">Requirement</span></span> | <span data-ttu-id="3a5fc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3a5fc-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5fc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a5fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5fc-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a5fc-120">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3a5fc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a5fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5fc-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a5fc-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3a5fc-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a5fc-123">Namespace</span></span><br/>                | <span data-ttu-id="3a5fc-124">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3a5fc-124">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3a5fc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3a5fc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a5fc-126"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a5fc-126"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a5fc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5fc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5fc-128"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5fc-128"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a5fc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a5fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5fc-130">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="3a5fc-130">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





