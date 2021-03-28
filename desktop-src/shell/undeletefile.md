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
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272321"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="0ce45-103">Указатель функции "FM- \_ Удаление \_ процедуры"</span><span class="sxs-lookup"><span data-stu-id="0ce45-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="0ce45-104">Задает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов, когда пользователь выбирает команду " **Отменить удаление** " в меню " **файл** ".</span><span class="sxs-lookup"><span data-stu-id="0ce45-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ce45-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="0ce45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ce45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ce45-107">*хвндовнер*</span><span class="sxs-lookup"><span data-stu-id="0ce45-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="0ce45-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="0ce45-108">Type: **HWND**</span></span>

<span data-ttu-id="0ce45-109">Обработчик окна для диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="0ce45-109">The window handle to File Manager.</span></span> <span data-ttu-id="0ce45-110">Библиотека DLL для отмены удаления должна использовать этот обработчик, чтобы указать окно владельца для любого диалогового окна или окна сообщения, которое может отображаться в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="0ce45-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="0ce45-111">*лпсздир*</span><span class="sxs-lookup"><span data-stu-id="0ce45-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="0ce45-112">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="0ce45-112">Type: **LPSTR**</span></span>

<span data-ttu-id="0ce45-113">Адрес строки, завершающейся нулем, которая содержит имя исходного каталога.</span><span class="sxs-lookup"><span data-stu-id="0ce45-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ce45-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ce45-114">Return value</span></span>

<span data-ttu-id="0ce45-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0ce45-115">Type: **DWORD**</span></span>

<span data-ttu-id="0ce45-116">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0ce45-116">Returns one of the following values.</span></span>



| <span data-ttu-id="0ce45-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0ce45-117">Return code</span></span>                                                                             | <span data-ttu-id="0ce45-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0ce45-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ce45-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="0ce45-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="0ce45-120">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="0ce45-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ce45-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ce45-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="0ce45-122">Файл был удален.</span><span class="sxs-lookup"><span data-stu-id="0ce45-122">A file was undeleted.</span></span> <span data-ttu-id="0ce45-123">Диспетчер файлов перерисовывает свое окно.</span><span class="sxs-lookup"><span data-stu-id="0ce45-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="0ce45-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="0ce45-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="0ce45-125">Файл не был удален.</span><span class="sxs-lookup"><span data-stu-id="0ce45-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="0ce45-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0ce45-126">Requirements</span></span>



| <span data-ttu-id="0ce45-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0ce45-127">Requirement</span></span> | <span data-ttu-id="0ce45-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0ce45-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce45-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ce45-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce45-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0ce45-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ce45-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ce45-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce45-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0ce45-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0ce45-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0ce45-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ce45-134"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce45-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




