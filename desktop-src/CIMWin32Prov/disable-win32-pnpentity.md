---
description: Отключает это устройство самонастраивающийся.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Метод Disable класса Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538699"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="0db68-103">Метод Disable \_ класса Win32 пнпентити</span><span class="sxs-lookup"><span data-stu-id="0db68-103">Disable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="0db68-104">Отключает это устройство самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="0db68-104">Disables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0db68-105">Syntax</span></span>


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="0db68-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0db68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db68-107">*ребутнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0db68-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db68-108">Необходимость перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="0db68-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0db68-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0db68-109">Requirements</span></span>



| <span data-ttu-id="0db68-110">Требование</span><span class="sxs-lookup"><span data-stu-id="0db68-110">Requirement</span></span> | <span data-ttu-id="0db68-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0db68-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db68-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0db68-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0db68-113">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0db68-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0db68-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0db68-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0db68-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0db68-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="0db68-116">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0db68-116">Namespace</span></span><br/>                | <span data-ttu-id="0db68-117">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0db68-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0db68-118">MOF</span><span class="sxs-lookup"><span data-stu-id="0db68-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0db68-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0db68-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0db68-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0db68-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db68-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db68-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db68-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0db68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db68-123">**\_Пнпентити Win32**</span><span class="sxs-lookup"><span data-stu-id="0db68-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




