---
description: Подклассировать все элементы управления в диалоговом окне и в самом диалоговом окне.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Функция Ctl3dSubclassDlgEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649033"
---
# <a name="ctl3dsubclassdlgex-function"></a><span data-ttu-id="62dc1-103">Функция Ctl3dSubclassDlgEx</span><span class="sxs-lookup"><span data-stu-id="62dc1-103">Ctl3dSubclassDlgEx function</span></span>

<span data-ttu-id="62dc1-104">Подклассировать все элементы управления в диалоговом окне и в самом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="62dc1-104">Subclasses all controls in a dialog box and in the dialog window itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="62dc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62dc1-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a><span data-ttu-id="62dc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62dc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62dc1-107">*хвнддлг*</span><span class="sxs-lookup"><span data-stu-id="62dc1-107">*hwndDlg*</span></span> 
</dt> <dd>

<span data-ttu-id="62dc1-108">Маркер диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="62dc1-108">A handle to the dialog window.</span></span>

</dd> <dt>

<span data-ttu-id="62dc1-109">*грбит*</span><span class="sxs-lookup"><span data-stu-id="62dc1-109">*grbit*</span></span> 
</dt> <dd>

<span data-ttu-id="62dc1-110">Типы элементов управления, которые должны быть подклассами.</span><span class="sxs-lookup"><span data-stu-id="62dc1-110">The control types to be subclassed.</span></span> <span data-ttu-id="62dc1-111">Это значение может быть любым из следующих.</span><span class="sxs-lookup"><span data-stu-id="62dc1-111">This value can be any of the following.</span></span>



| <span data-ttu-id="62dc1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="62dc1-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="62dc1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="62dc1-113">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <span data-ttu-id="62dc1-114"><dt>**CTL3D сегодня \_ КНОПКИ**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-114"><dt>**CTL3D\_BUTTONS**</dt> <dt>0x0001</dt></span></span> </dl>                 | <span data-ttu-id="62dc1-115">Кнопки подклассов.</span><span class="sxs-lookup"><span data-stu-id="62dc1-115">Subclass buttons.</span></span><br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <span data-ttu-id="62dc1-116"><dt>**CTL3D сегодня \_ СПИСКИ**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-116"><dt>**CTL3D\_LISTBOXES**</dt> <dt>0x0002</dt></span></span> </dl>           | <span data-ttu-id="62dc1-117">Списки подклассов.</span><span class="sxs-lookup"><span data-stu-id="62dc1-117">Subclass list boxes.</span></span><br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <span data-ttu-id="62dc1-118"><dt>**CTL3D сегодня \_ РЕДАКТИРУЕТ**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-118"><dt>**CTL3D\_EDITS**</dt> <dt>0x0004</dt></span></span> </dl>                       | <span data-ttu-id="62dc1-119">Элементы управления редактированием подклассов.</span><span class="sxs-lookup"><span data-stu-id="62dc1-119">Subclass edit controls.</span></span><br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <span data-ttu-id="62dc1-120"><dt>**CTL3D сегодня \_ КомБОС**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-120"><dt>**CTL3D\_COMBOS**</dt> <dt>0x0008</dt></span></span> </dl>                    | <span data-ttu-id="62dc1-121">Поля со списком подклассов.</span><span class="sxs-lookup"><span data-stu-id="62dc1-121">Subclass combo boxes.</span></span><br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <span data-ttu-id="62dc1-122"><dt>**CTL3D сегодня \_ СТАТИКТЕКСТС**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-122"><dt>**CTL3D\_STATICTEXTS**</dt> <dt>0x0010</dt></span></span> </dl>     | <span data-ttu-id="62dc1-123">Подклассировать статические текстовые элементы управления.</span><span class="sxs-lookup"><span data-stu-id="62dc1-123">Subclass static text controls.</span></span><br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <span data-ttu-id="62dc1-124"><dt>**CTL3D сегодня \_ СТАТИКФРАМЕС**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-124"><dt>**CTL3D\_STATICFRAMES**</dt> <dt>0x0020</dt></span></span> </dl>  | <span data-ttu-id="62dc1-125">Создать подкласс для статических фреймов.</span><span class="sxs-lookup"><span data-stu-id="62dc1-125">Subclass static frames.</span></span><br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <span data-ttu-id="62dc1-126"><dt>**CTL3D сегодня \_ ВСЕ**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-126"><dt>**CTL3D\_ALL**</dt> <dt>0xffff</dt></span></span> </dl>                             | <span data-ttu-id="62dc1-127">Подкласс все элементы управления.</span><span class="sxs-lookup"><span data-stu-id="62dc1-127">Subclass all controls.</span></span><br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <span data-ttu-id="62dc1-128"><dt>**CTL3D сегодня \_ НОДЛГВИНДОВ**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-128"><dt>**CTL3D\_NODLGWINDOW**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="62dc1-129">Не подделать подкласс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="62dc1-129">Do not subclass the dialog window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62dc1-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62dc1-130">Return value</span></span>

<span data-ttu-id="62dc1-131">Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62dc1-131">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62dc1-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62dc1-132">Remarks</span></span>

<span data-ttu-id="62dc1-133">Эта функция особенно полезна в приложениях, основанных на C++.</span><span class="sxs-lookup"><span data-stu-id="62dc1-133">This function is especially useful in applications based on C++.</span></span>

<span data-ttu-id="62dc1-134">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="62dc1-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="62dc1-135">Требования</span><span class="sxs-lookup"><span data-stu-id="62dc1-135">Requirements</span></span>



| <span data-ttu-id="62dc1-136">Требование</span><span class="sxs-lookup"><span data-stu-id="62dc1-136">Requirement</span></span> | <span data-ttu-id="62dc1-137">Значение</span><span class="sxs-lookup"><span data-stu-id="62dc1-137">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62dc1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="62dc1-138">DLL</span></span><br/> | <dl> <span data-ttu-id="62dc1-139"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62dc1-139"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
