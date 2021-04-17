---
title: Метод Енаблеусервхд класса Win32_TSSessionDirectory
description: Включает виртуальный жесткий диск профиля пользователя на сервере узлов удаленных рабочих столов.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблеусервхд
- Службы удаленных рабочих столов метода Енаблеусервхд, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Енаблеусервхд
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682149"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="161b3-106">Метод Енаблеусервхд \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="161b3-106">EnableUserVhd method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="161b3-107">Включает виртуальный жесткий диск профиля пользователя на сервере узлов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="161b3-107">Enables a user profile VHD on an RDSH server.</span></span>

## <a name="syntax"></a><span data-ttu-id="161b3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="161b3-108">Syntax</span></span>


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a><span data-ttu-id="161b3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="161b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="161b3-110">*Увхдшареурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="161b3-110">*UvhdShareUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161b3-111">Расположение общей папки, в которой хранятся все виртуальные жесткие диски профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="161b3-111">The location of the share where all user profile VHDs are stored.</span></span>

</dd> <dt>

<span data-ttu-id="161b3-112">*Увхдроамингполициксмл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="161b3-112">*UvhdRoamingPolicyXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161b3-113">Политика роуминга для виртуального жесткого диска профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="161b3-113">The roaming policy for the user profile VHD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="161b3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="161b3-114">Requirements</span></span>



| <span data-ttu-id="161b3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="161b3-115">Requirement</span></span> | <span data-ttu-id="161b3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="161b3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="161b3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="161b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="161b3-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="161b3-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="161b3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="161b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="161b3-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="161b3-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="161b3-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="161b3-121">Namespace</span></span><br/>                | <span data-ttu-id="161b3-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="161b3-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="161b3-123">MOF</span><span class="sxs-lookup"><span data-stu-id="161b3-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="161b3-124"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="161b3-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="161b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="161b3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="161b3-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="161b3-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="161b3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="161b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="161b3-128">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="161b3-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





