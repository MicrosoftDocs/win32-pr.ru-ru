---
description: Запрашивает драйвер для дополнительных функций Microsoft DirectDraw и Microsoft Direct3D, поддерживаемых драйвером.
ms.assetid: 7169b672-5c61-4fca-860b-5ef426a7f925
title: Функция Нтгдидджетдриверинфо (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDriverInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2e9f78ed832015979c6768ec8f09e53ca8d2d4a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496200"
---
# <a name="ntgdiddgetdriverinfo-function"></a><span data-ttu-id="9c6bb-103">Функция Нтгдидджетдриверинфо</span><span class="sxs-lookup"><span data-stu-id="9c6bb-103">NtGdiDdGetDriverInfo function</span></span>

<span data-ttu-id="9c6bb-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9c6bb-105">Вместо этого используйте DirectDraw и Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="9c6bb-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9c6bb-106">Запрашивает драйвер для дополнительных функций Microsoft DirectDraw и Microsoft Direct3D, поддерживаемых драйвером.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-106">Queries the driver for additional Microsoft DirectDraw and Microsoft Direct3D functionality that the driver supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6bb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c6bb-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDriverInfo(
  _In_    HANDLE                hDirectDraw,
  _Inout_ PDD_GETDRIVERINFODATA puGetDriverInfoData
);
```



## <a name="parameters"></a><span data-ttu-id="9c6bb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c6bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c6bb-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c6bb-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6bb-110">Обработчик для ранее созданного объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="9c6bb-111">*пужетдриверинфодата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9c6bb-111">*puGetDriverInfoData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6bb-112">Указатель на структуру [DD \_ жетдриверинфодата](https://msdn.microsoft.com/library/ms793868.aspx) , которая содержит сведения, необходимые для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-112">Pointer to a [DD\_GETDRIVERINFODATA](https://msdn.microsoft.com/library/ms793868.aspx) structure that contains the information required to perform the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c6bb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c6bb-113">Return value</span></span>

<span data-ttu-id="9c6bb-114">**Нтгдидджетдриверинфо** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-114">**NtGdiDdGetDriverInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9c6bb-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c6bb-115">Return code</span></span>                                                                                              | <span data-ttu-id="9c6bb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9c6bb-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c6bb-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="9c6bb-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9c6bb-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9c6bb-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9c6bb-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9c6bb-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="9c6bb-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9c6bb-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9c6bb-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9c6bb-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="9c6bb-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9c6bb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9c6bb-125">Requirements</span></span>



| <span data-ttu-id="9c6bb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9c6bb-126">Requirement</span></span> | <span data-ttu-id="9c6bb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9c6bb-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6bb-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c6bb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6bb-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c6bb-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9c6bb-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c6bb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6bb-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c6bb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c6bb-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c6bb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c6bb-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6bb-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6bb-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c6bb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6bb-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="9c6bb-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




