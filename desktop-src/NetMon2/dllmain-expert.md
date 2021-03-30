---
description: Эксперт реализует функцию DllMain. Операционная система вызывает функцию DllMain для получения маркера экземпляра эксперта.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Функция обратного вызова DllMain эксперта (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910888"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="acf71-104">Функция обратного вызова DllMain эксперта</span><span class="sxs-lookup"><span data-stu-id="acf71-104">DllMain Expert callback function</span></span>

<span data-ttu-id="acf71-105">Эксперт реализует функцию [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="acf71-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="acf71-106">Операционная система вызывает функцию **DllMain** для получения маркера экземпляра эксперта.</span><span class="sxs-lookup"><span data-stu-id="acf71-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf71-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acf71-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="acf71-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="acf71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf71-109">*HINSTANCE* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acf71-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf71-110">Обработайте с экземпляром эксперта.</span><span class="sxs-lookup"><span data-stu-id="acf71-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="acf71-111">Если эксперт использует сетевой монитор пользовательский интерфейс, значение *HINSTANCE* должно храниться в глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="acf71-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="acf71-112">Этот подход необходим только в том случае, если для параметра *улреасон* задано значение DLL \_ Process \_ Attach.</span><span class="sxs-lookup"><span data-stu-id="acf71-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="acf71-113">*улреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acf71-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf71-114">Признак вызова функции.</span><span class="sxs-lookup"><span data-stu-id="acf71-114">Indicator of why the function was called.</span></span> <span data-ttu-id="acf71-115">Значение параметра \_ \_ присоединение процесса DLL (которое применяется при первой загрузке библиотеки DLL) указывает, что эксперт должен сохранить значение *HINSTANCE* в глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="acf71-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="acf71-116">При любом другом значении все вызовы функции [**DllMain**](/windows/desktop/Dlls/dllmain) можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="acf71-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="acf71-117">Список всех возможных флагов, установленных операционной системой, см. в разделе **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="acf71-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="acf71-118">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="acf71-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="acf71-119">Параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="acf71-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf71-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acf71-120">Return value</span></span>

<span data-ttu-id="acf71-121">Если функция выполнена успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="acf71-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="acf71-122">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="acf71-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf71-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acf71-123">Remarks</span></span>

<span data-ttu-id="acf71-124">Операционная система вызывает функцию эксперта **DllMain** , когда процесс загружает или ВЫГРУЖАЕТ библиотеку DLL эксперта.</span><span class="sxs-lookup"><span data-stu-id="acf71-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="acf71-125">Функция **DllMain** эксперта должна быть экспортирована только в том случае, если эксперт имеет пользовательский интерфейс для просмотра конфигурации или результатов, а затем только возвращает правильное значение *HINSTANCE* .</span><span class="sxs-lookup"><span data-stu-id="acf71-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="acf71-126">Функция **DllMain** , созданная на основе функции [**DllMain**](/windows/desktop/Dlls/dllmain) библиотеки динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="acf71-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf71-127">Требования</span><span class="sxs-lookup"><span data-stu-id="acf71-127">Requirements</span></span>



| <span data-ttu-id="acf71-128">Требование</span><span class="sxs-lookup"><span data-stu-id="acf71-128">Requirement</span></span> | <span data-ttu-id="acf71-129">Значение</span><span class="sxs-lookup"><span data-stu-id="acf71-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="acf71-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acf71-130">Minimum supported client</span></span><br/> | <span data-ttu-id="acf71-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acf71-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="acf71-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acf71-132">Minimum supported server</span></span><br/> | <span data-ttu-id="acf71-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acf71-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="acf71-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="acf71-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="acf71-135"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="acf71-135"><dt>Process.h</dt></span></span> </dl> |



 

