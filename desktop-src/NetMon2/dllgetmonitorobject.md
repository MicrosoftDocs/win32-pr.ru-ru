---
description: Функция Дллжетмониторобжект должна быть реализована монитором. МКСВК вызывает эту функцию для создания экземпляра монитора.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Функция обратного вызова Дллжетмониторобжект (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912840"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="73916-104">Функция обратного вызова Дллжетмониторобжект</span><span class="sxs-lookup"><span data-stu-id="73916-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="73916-105">Функция **дллжетмониторобжект** должна быть реализована монитором.</span><span class="sxs-lookup"><span data-stu-id="73916-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="73916-106">МКСВК вызывает эту функцию для создания экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="73916-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="73916-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73916-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="73916-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="73916-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73916-109">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73916-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73916-110">UUID мониторов, показанный ниже, как определено в файле заголовка Имонитор. h.</span><span class="sxs-lookup"><span data-stu-id="73916-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="73916-111">Если указан недопустимый UUID, функция завершается ошибкой, а монитор должен возвращать E- \_ интерфейс.</span><span class="sxs-lookup"><span data-stu-id="73916-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="73916-112">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73916-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73916-113">Указатель на указатель, который получает интерфейс, запрошенный в *riid*.</span><span class="sxs-lookup"><span data-stu-id="73916-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73916-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73916-114">Return value</span></span>

<span data-ttu-id="73916-115">Если функция выполнена успешно, возвращается значение S \_ OK (то же самое, что и ошибка).</span><span class="sxs-lookup"><span data-stu-id="73916-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="73916-116">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="73916-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="73916-117">При возвращении кода ошибки МКСВК не создает объект Monitor, а метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) не вызывается для указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="73916-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="73916-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73916-118">Remarks</span></span>

<span data-ttu-id="73916-119">Функция **дллжетмониторобжект** вызывается каждый раз, когда мксвк пытается создать экземпляр монитора.</span><span class="sxs-lookup"><span data-stu-id="73916-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="73916-120">Эта функция намеренно несет серьезную сходство с наиболее распространенной функцией [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) .</span><span class="sxs-lookup"><span data-stu-id="73916-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="73916-121">Основное отличие заключается в том, что CLSID не передается в **дллжетмониторобжект**.</span><span class="sxs-lookup"><span data-stu-id="73916-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="73916-122">Требования</span><span class="sxs-lookup"><span data-stu-id="73916-122">Requirements</span></span>



| <span data-ttu-id="73916-123">Требование</span><span class="sxs-lookup"><span data-stu-id="73916-123">Requirement</span></span> | <span data-ttu-id="73916-124">Значение</span><span class="sxs-lookup"><span data-stu-id="73916-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="73916-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73916-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73916-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="73916-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="73916-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73916-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73916-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="73916-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="73916-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="73916-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="73916-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="73916-130"><dt>Netmon.h</dt></span></span> </dl> |



 

