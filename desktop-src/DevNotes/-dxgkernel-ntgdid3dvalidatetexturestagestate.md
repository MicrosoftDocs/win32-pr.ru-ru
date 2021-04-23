---
description: Возвращает число проходов, в которых оборудование может выполнять операции смешения, указанные в текущем состоянии.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: Функция NtGdiD3DValidateTextureStageState (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 37c852343c70c5d3325926c9108dcab2948fdc95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895582"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a><span data-ttu-id="e65fa-103">Функция NtGdiD3DValidateTextureStageState</span><span class="sxs-lookup"><span data-stu-id="e65fa-103">NtGdiD3DValidateTextureStageState function</span></span>

<span data-ttu-id="e65fa-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e65fa-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e65fa-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="e65fa-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e65fa-106">Возвращает число проходов, в которых оборудование может выполнять операции смешения, указанные в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="e65fa-106">Returns the number of passes where the hardware can perform the blending operations specified in the current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e65fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e65fa-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="e65fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e65fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e65fa-109">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e65fa-109">*pData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e65fa-110">Указатель на структуру [**\_ валидатетекстурестажестатедата D3DNTHAL**](/windows-hardware/drivers/ddi/) , которая содержит сведения, необходимые драйверу для определения и возврата количества проходов, необходимых для выполнения операций смешения.</span><span class="sxs-lookup"><span data-stu-id="e65fa-110">Pointer to a [**D3DNTHAL\_VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to determine and return the number of passes required to perform the blending operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e65fa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e65fa-111">Return value</span></span>

<span data-ttu-id="e65fa-112">**NtGdiD3DValidateTextureStageState** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e65fa-112">**NtGdiD3DValidateTextureStageState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e65fa-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e65fa-113">Return code</span></span>                                                                                              | <span data-ttu-id="e65fa-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e65fa-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e65fa-115"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="e65fa-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e65fa-116">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="e65fa-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e65fa-117">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="e65fa-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e65fa-118">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="e65fa-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e65fa-119"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="e65fa-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e65fa-120">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="e65fa-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e65fa-121">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e65fa-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e65fa-122">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="e65fa-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e65fa-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e65fa-123">Requirements</span></span>



| <span data-ttu-id="e65fa-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e65fa-124">Requirement</span></span> | <span data-ttu-id="e65fa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e65fa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e65fa-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e65fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e65fa-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e65fa-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e65fa-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e65fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e65fa-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e65fa-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e65fa-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e65fa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e65fa-131"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="e65fa-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e65fa-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e65fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65fa-133">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="e65fa-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
