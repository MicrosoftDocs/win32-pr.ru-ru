---
description: Метод Delete класса Win32_SystemDriver — удаление&\# 8194; Метод класса WMI удаляет существующую службу.
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Метод Delete класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097092"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="4519a-103">Метод DELETE \_ класса SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="4519a-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="4519a-104">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="4519a-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="4519a-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4519a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4519a-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4519a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4519a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4519a-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="4519a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4519a-108">Parameters</span></span>

<span data-ttu-id="4519a-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4519a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4519a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4519a-110">Return value</span></span>

<span data-ttu-id="4519a-111">Возвращает значение 0 (нуль), если служба была успешно удалена, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="4519a-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4519a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4519a-112">Requirements</span></span>



| <span data-ttu-id="4519a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4519a-113">Requirement</span></span> | <span data-ttu-id="4519a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4519a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4519a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4519a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4519a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4519a-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4519a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4519a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4519a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4519a-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4519a-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4519a-119">Namespace</span></span><br/>                | <span data-ttu-id="4519a-120">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4519a-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4519a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="4519a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4519a-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4519a-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4519a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4519a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4519a-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4519a-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4519a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4519a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4519a-126">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4519a-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4519a-127">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="4519a-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

