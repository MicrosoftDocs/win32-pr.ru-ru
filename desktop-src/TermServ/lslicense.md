---
title: Структура Лслиценсе
description: Содержит сведения о конкретной лицензии службы удаленных рабочих столов.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов структуры Лслиценсе
- службы удаленных рабочих столов указателя структуры Лплслиценсе
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490332"
---
# <a name="lslicense-structure"></a><span data-ttu-id="98078-105">Структура Лслиценсе</span><span class="sxs-lookup"><span data-stu-id="98078-105">LSLicense structure</span></span>

<span data-ttu-id="98078-106">Содержит сведения о конкретной лицензии службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="98078-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="98078-107">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="98078-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="98078-108">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="98078-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="98078-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98078-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="98078-110">Члены</span><span class="sxs-lookup"><span data-stu-id="98078-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="98078-111">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="98078-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="98078-112">Версия лицензии.</span><span class="sxs-lookup"><span data-stu-id="98078-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-113">**двлиценсеид**</span><span class="sxs-lookup"><span data-stu-id="98078-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="98078-114">Идентификатор лицензии.</span><span class="sxs-lookup"><span data-stu-id="98078-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-115">**двкэйпаккид**</span><span class="sxs-lookup"><span data-stu-id="98078-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="98078-116">Идентификатор [**лскэйпакк**](lskeypack.md) , который содержит лицензию.</span><span class="sxs-lookup"><span data-stu-id="98078-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-117">**сзвид**</span><span class="sxs-lookup"><span data-stu-id="98078-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="98078-118">Идентификатор оборудования клиента подключение к удаленному рабочему столу (RDC), который выдал лицензию.</span><span class="sxs-lookup"><span data-stu-id="98078-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-119">**сзмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="98078-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="98078-120">Имя клиента подключение к удаленному рабочему столу (RDC), который выдал лицензию.</span><span class="sxs-lookup"><span data-stu-id="98078-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-121">**сзусернаме**</span><span class="sxs-lookup"><span data-stu-id="98078-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="98078-122">Имя пользователя, который выдал лицензию.</span><span class="sxs-lookup"><span data-stu-id="98078-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-123">**двцертсериаллиценсе**</span><span class="sxs-lookup"><span data-stu-id="98078-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="98078-124">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="98078-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="98078-125">**двлиценсесериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="98078-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="98078-126">Серийный номер лицензии.</span><span class="sxs-lookup"><span data-stu-id="98078-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="98078-127">**фтиссуедате**</span><span class="sxs-lookup"><span data-stu-id="98078-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="98078-128">Дата выдачи лицензии.</span><span class="sxs-lookup"><span data-stu-id="98078-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="98078-129">**фтекспиредате**</span><span class="sxs-lookup"><span data-stu-id="98078-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="98078-130">Дата истечения срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="98078-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="98078-131">**уклиценсестатус**</span><span class="sxs-lookup"><span data-stu-id="98078-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="98078-132">Текущее состояние лицензии.</span><span class="sxs-lookup"><span data-stu-id="98078-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98078-133">Требования</span><span class="sxs-lookup"><span data-stu-id="98078-133">Requirements</span></span>



| <span data-ttu-id="98078-134">Требование</span><span class="sxs-lookup"><span data-stu-id="98078-134">Requirement</span></span> | <span data-ttu-id="98078-135">Значение</span><span class="sxs-lookup"><span data-stu-id="98078-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="98078-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98078-136">Minimum supported client</span></span><br/> | <span data-ttu-id="98078-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98078-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="98078-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98078-138">Minimum supported server</span></span><br/> | <span data-ttu-id="98078-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98078-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98078-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98078-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98078-141">**лскэйпакк**</span><span class="sxs-lookup"><span data-stu-id="98078-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="98078-142">**тлслиценсинумбегин**</span><span class="sxs-lookup"><span data-stu-id="98078-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="98078-143">**тлслиценсинумнекст**</span><span class="sxs-lookup"><span data-stu-id="98078-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="98078-144">**тлслиценсинуменд**</span><span class="sxs-lookup"><span data-stu-id="98078-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





