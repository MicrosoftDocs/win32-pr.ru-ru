---
description: Определяет расположение ресурса с указанным типом и именем в указанном модуле.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Функция Финдресаурцеврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264437"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="a480d-103">Функция Финдресаурцеврапв</span><span class="sxs-lookup"><span data-stu-id="a480d-103">FindResourceWrapW function</span></span>

<span data-ttu-id="a480d-104">\[**Финдресаурцеврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a480d-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="a480d-105">Она может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="a480d-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="a480d-106">Вместо этого следует использовать [**финдресаурцев**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]</span><span class="sxs-lookup"><span data-stu-id="a480d-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="a480d-107">Определяет расположение ресурса с указанным типом и именем в указанном модуле.</span><span class="sxs-lookup"><span data-stu-id="a480d-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="a480d-108">**Финдресаурцеврапв** — это оболочка для функции **финдресаурцев** .</span><span class="sxs-lookup"><span data-stu-id="a480d-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="a480d-109">Дополнительные замечания об использовании см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .</span><span class="sxs-lookup"><span data-stu-id="a480d-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a480d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a480d-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="a480d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a480d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a480d-112">*хмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a480d-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a480d-113">Тип: **хмодуле**</span><span class="sxs-lookup"><span data-stu-id="a480d-113">Type: **HMODULE**</span></span>

<span data-ttu-id="a480d-114">Обработчик для модуля, исполняемый файл которого содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="a480d-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="a480d-115">Значение **null** указывает маркер модуля, связанный с файлом образа, который используется операционной системой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="a480d-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="a480d-116">*лпнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a480d-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a480d-117">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="a480d-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="a480d-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a480d-118">The name of the resource.</span></span> <span data-ttu-id="a480d-119">Дополнительные сведения см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="a480d-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="a480d-120">*лптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a480d-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a480d-121">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="a480d-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="a480d-122">Указатель на строку, указывающую тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="a480d-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="a480d-123">Дополнительные сведения см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="a480d-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a480d-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a480d-124">Return value</span></span>

<span data-ttu-id="a480d-125">Тип: **хрсрк**</span><span class="sxs-lookup"><span data-stu-id="a480d-125">Type: **HRSRC**</span></span>

<span data-ttu-id="a480d-126">Если функция выполнена, возвращаемое значение является маркером для блока сведений указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a480d-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="a480d-127">Чтобы получить маркер для ресурса, передайте этот обработчик функции [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="a480d-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="a480d-128">Если функция завершается ошибкой, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a480d-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="a480d-129">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="a480d-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="a480d-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="a480d-130">Remarks</span></span>

<span data-ttu-id="a480d-131">Если необходимо указать определенную локализацию, используйте функцию [**финдресаурцеекс**](/windows/win32/api/winbase/nf-winbase-findresourceexa) , а не **финдресаурцеврапв**.</span><span class="sxs-lookup"><span data-stu-id="a480d-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="a480d-132">**Финдресаурцеврапв** предоставляет возможность использования строк Юникода в более старых операционных системах.</span><span class="sxs-lookup"><span data-stu-id="a480d-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="a480d-133">Предпочтительным методом является использование [**финдресаурцев**](/windows/win32/api/winbase/nf-winbase-findresourcea) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="a480d-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="a480d-134">**Финдресаурцеврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 66.</span><span class="sxs-lookup"><span data-stu-id="a480d-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="a480d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a480d-135">Requirements</span></span>



| <span data-ttu-id="a480d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a480d-136">Requirement</span></span> | <span data-ttu-id="a480d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a480d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a480d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a480d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a480d-139">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a480d-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a480d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a480d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a480d-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a480d-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a480d-142">Header</span><span class="sxs-lookup"><span data-stu-id="a480d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a480d-143"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="a480d-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="a480d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a480d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a480d-145"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a480d-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="a480d-146">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a480d-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a480d-147">**Финдресаурцеврапв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="a480d-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="a480d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a480d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a480d-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="a480d-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
