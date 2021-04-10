---
title: Метод Креатеусердисктемплате класса Win32_TSSessionDirectory
description: Создает шаблон диска пользователя.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатеусердисктемплате
- Службы удаленных рабочих столов метода Креатеусердисктемплате, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Креатеусердисктемплате
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135331"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="7b09f-106">Метод Креатеусердисктемплате \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="7b09f-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="7b09f-107">Создает шаблон диска пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b09f-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b09f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b09f-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="7b09f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b09f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b09f-110">*Усердискссторажеурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b09f-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b09f-111">Расположение общей папки, в которой хранятся все диски пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b09f-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="7b09f-112">*Усердискмакссизеингб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b09f-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b09f-113">Максимальный размер (в гигабайтах) для всех дисков пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b09f-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b09f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7b09f-114">Requirements</span></span>



| <span data-ttu-id="7b09f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7b09f-115">Requirement</span></span> | <span data-ttu-id="7b09f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7b09f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b09f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b09f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b09f-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b09f-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7b09f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b09f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b09f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b09f-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="7b09f-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b09f-121">Namespace</span></span><br/>                | <span data-ttu-id="7b09f-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7b09f-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7b09f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7b09f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b09f-124"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b09f-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b09f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7b09f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b09f-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b09f-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b09f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b09f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b09f-128">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="7b09f-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





