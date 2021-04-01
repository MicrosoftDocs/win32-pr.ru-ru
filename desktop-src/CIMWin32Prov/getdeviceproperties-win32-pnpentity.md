---
description: Возвращает указанные свойства данного устройства самонастраивающийся.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Метод Жетдевицепропертиес класса Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072413"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="57622-103">Метод Жетдевицепропертиес \_ класса Win32 пнпентити</span><span class="sxs-lookup"><span data-stu-id="57622-103">GetDeviceProperties method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="57622-104">Возвращает указанные свойства данного устройства самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="57622-104">Gets the specified properties of this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="57622-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57622-105">Syntax</span></span>


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a><span data-ttu-id="57622-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57622-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57622-107">*девицепропертикэйс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="57622-107">*devicePropertyKeys* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="57622-108">Возвращаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="57622-108">The properties to return.</span></span>

</dd> <dt>

<span data-ttu-id="57622-109">*девицепропертиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="57622-109">*deviceProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57622-110">Запрошенные свойства в соответствующих подтипах абстрактного класса [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="57622-110">The requested properties in appropriate subtypes of the [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md) abstract class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57622-111">Требования</span><span class="sxs-lookup"><span data-stu-id="57622-111">Requirements</span></span>



| <span data-ttu-id="57622-112">Требование</span><span class="sxs-lookup"><span data-stu-id="57622-112">Requirement</span></span> | <span data-ttu-id="57622-113">Значение</span><span class="sxs-lookup"><span data-stu-id="57622-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57622-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57622-114">Minimum supported client</span></span><br/> | <span data-ttu-id="57622-115">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="57622-115">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="57622-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57622-116">Minimum supported server</span></span><br/> | <span data-ttu-id="57622-117">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="57622-117">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="57622-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="57622-118">Namespace</span></span><br/>                | <span data-ttu-id="57622-119">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="57622-119">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57622-120">MOF</span><span class="sxs-lookup"><span data-stu-id="57622-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57622-121"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57622-121"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57622-122">DLL</span><span class="sxs-lookup"><span data-stu-id="57622-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57622-123"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57622-123"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57622-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57622-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57622-125">**\_Пнпентити Win32**</span><span class="sxs-lookup"><span data-stu-id="57622-125">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




