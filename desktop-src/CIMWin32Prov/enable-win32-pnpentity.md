---
description: Включает это самонастраивающийся устройство.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Enable, метод класса Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655803"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="17da5-103">Enable, метод класса Win32 \_ пнпентити</span><span class="sxs-lookup"><span data-stu-id="17da5-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="17da5-104">Включает это самонастраивающийся устройство.</span><span class="sxs-lookup"><span data-stu-id="17da5-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="17da5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17da5-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="17da5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17da5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17da5-107">*ребутнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17da5-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17da5-108">Необходимость перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="17da5-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17da5-109">Требования</span><span class="sxs-lookup"><span data-stu-id="17da5-109">Requirements</span></span>



| <span data-ttu-id="17da5-110">Требование</span><span class="sxs-lookup"><span data-stu-id="17da5-110">Requirement</span></span> | <span data-ttu-id="17da5-111">Значение</span><span class="sxs-lookup"><span data-stu-id="17da5-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17da5-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17da5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="17da5-113">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="17da5-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="17da5-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17da5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="17da5-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="17da5-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="17da5-116">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="17da5-116">Namespace</span></span><br/>                | <span data-ttu-id="17da5-117">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17da5-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17da5-118">MOF</span><span class="sxs-lookup"><span data-stu-id="17da5-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17da5-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17da5-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17da5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="17da5-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17da5-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17da5-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17da5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17da5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17da5-123">**\_Пнпентити Win32**</span><span class="sxs-lookup"><span data-stu-id="17da5-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




