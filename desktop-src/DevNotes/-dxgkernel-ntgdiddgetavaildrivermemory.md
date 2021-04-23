---
description: Запрашивает объем свободной памяти во всех кучах видеопамяти.
ms.assetid: 6718e8da-0da0-42e3-a02b-6884b141fe24
title: Функция Нтгдидджетаваилдривермемори (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetAvailDriverMemory
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c6ec322665b84b3ddad14b7032b8e49245377d40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072440"
---
# <a name="ntgdiddgetavaildrivermemory-function"></a><span data-ttu-id="f5514-103">Функция Нтгдидджетаваилдривермемори</span><span class="sxs-lookup"><span data-stu-id="f5514-103">NtGdiDdGetAvailDriverMemory function</span></span>

<span data-ttu-id="f5514-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f5514-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f5514-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="f5514-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f5514-106">Запрашивает объем свободной памяти во всех кучах видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="f5514-106">Queries the amount of free memory in all video memory heaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5514-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5514-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetAvailDriverMemory(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_GETAVAILDRIVERMEMORYDATA puGetAvailDriverMemoryData
);
```



## <a name="parameters"></a><span data-ttu-id="f5514-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5514-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5514-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5514-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5514-110">Обработчик для ранее созданного объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="f5514-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="f5514-111">*пужетаваилдривермеморидата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f5514-111">*puGetAvailDriverMemoryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5514-112">Указатель на структуру [DD \_ жетаваилдривермеморидата](https://msdn.microsoft.com/library/ms794088.aspx) , которая содержит сведения, необходимые для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="f5514-112">Pointer to a [DD\_GETAVAILDRIVERMEMORYDATA](https://msdn.microsoft.com/library/ms794088.aspx) structure that contains the information required to perform the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5514-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5514-113">Return value</span></span>

<span data-ttu-id="f5514-114">**Нтгдидджетаваилдривермемори** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f5514-114">**NtGdiDdGetAvailDriverMemory** returns one of the following callback codes.</span></span>



| <span data-ttu-id="f5514-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f5514-115">Return code</span></span>                                                                                              | <span data-ttu-id="f5514-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f5514-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5514-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="f5514-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="f5514-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="f5514-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="f5514-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="f5514-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="f5514-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="f5514-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f5514-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="f5514-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="f5514-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="f5514-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="f5514-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f5514-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="f5514-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="f5514-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f5514-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f5514-125">Requirements</span></span>



| <span data-ttu-id="f5514-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f5514-126">Requirement</span></span> | <span data-ttu-id="f5514-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f5514-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5514-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5514-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5514-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5514-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f5514-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5514-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5514-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5514-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5514-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f5514-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5514-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5514-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5514-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5514-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5514-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="f5514-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




