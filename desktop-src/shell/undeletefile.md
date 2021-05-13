---
description: Задает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов, когда пользователь выбирает команду "отменить удаление" в меню "файл".
title: Указатель функции FM_UNDELETE_PROC (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842425"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="d4087-103">Указатель функции "FM- \_ Удаление \_ процедуры"</span><span class="sxs-lookup"><span data-stu-id="d4087-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="d4087-104">Задает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов, когда пользователь выбирает команду " **Отменить удаление** " в меню " **файл** ".</span><span class="sxs-lookup"><span data-stu-id="d4087-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4087-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4087-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="d4087-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4087-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4087-107">*хвндовнер*</span><span class="sxs-lookup"><span data-stu-id="d4087-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="d4087-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d4087-108">Type: **HWND**</span></span>

<span data-ttu-id="d4087-109">Обработчик окна для диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="d4087-109">The window handle to File Manager.</span></span> <span data-ttu-id="d4087-110">Библиотека DLL для отмены удаления должна использовать этот обработчик, чтобы указать окно владельца для любого диалогового окна или окна сообщения, которое может отображаться в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d4087-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="d4087-111">*лпсздир*</span><span class="sxs-lookup"><span data-stu-id="d4087-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="d4087-112">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d4087-112">Type: **LPSTR**</span></span>

<span data-ttu-id="d4087-113">Адрес строки, завершающейся нулем, которая содержит имя исходного каталога.</span><span class="sxs-lookup"><span data-stu-id="d4087-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4087-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4087-114">Return value</span></span>

<span data-ttu-id="d4087-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d4087-115">Type: **DWORD**</span></span>

<span data-ttu-id="d4087-116">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d4087-116">Returns one of the following values.</span></span>



| <span data-ttu-id="d4087-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d4087-117">Return code</span></span>                                                                             | <span data-ttu-id="d4087-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d4087-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4087-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="d4087-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="d4087-120">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="d4087-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d4087-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4087-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="d4087-122">Файл был удален.</span><span class="sxs-lookup"><span data-stu-id="d4087-122">A file was undeleted.</span></span> <span data-ttu-id="d4087-123">Диспетчер файлов перерисовывает свое окно.</span><span class="sxs-lookup"><span data-stu-id="d4087-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="d4087-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="d4087-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="d4087-125">Файл не был удален.</span><span class="sxs-lookup"><span data-stu-id="d4087-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="d4087-126">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="d4087-126">Requirements</span></span>



| <span data-ttu-id="d4087-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d4087-127">Requirement</span></span> | <span data-ttu-id="d4087-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d4087-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4087-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4087-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d4087-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4087-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4087-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4087-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d4087-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4087-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d4087-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d4087-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4087-134"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4087-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




