---
description: Запрашивает обновление состояния службы системных драйверов до Service Manager.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Метод Интеррогатесервице класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141306"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="cecde-103">Метод Интеррогатесервице \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="cecde-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="cecde-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) интеррогатесервице запрашивает, чтобы служба драйвера системы запросила состояние обновления Service Manager.</span><span class="sxs-lookup"><span data-stu-id="cecde-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="cecde-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cecde-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cecde-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cecde-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cecde-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cecde-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="cecde-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cecde-108">Parameters</span></span>

<span data-ttu-id="cecde-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cecde-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cecde-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cecde-110">Return value</span></span>

<span data-ttu-id="cecde-111">Возвращает значение 0 (ноль), если запрос **интеррогатесервице** был принят, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="cecde-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cecde-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cecde-112">Requirements</span></span>



| <span data-ttu-id="cecde-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cecde-113">Requirement</span></span> | <span data-ttu-id="cecde-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cecde-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cecde-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cecde-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cecde-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cecde-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cecde-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cecde-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cecde-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cecde-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cecde-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cecde-119">Namespace</span></span><br/>                | <span data-ttu-id="cecde-120">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cecde-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cecde-121">MOF</span><span class="sxs-lookup"><span data-stu-id="cecde-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cecde-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cecde-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cecde-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cecde-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cecde-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cecde-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cecde-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cecde-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cecde-126">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="cecde-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="cecde-127">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cecde-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cecde-128">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="cecde-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

