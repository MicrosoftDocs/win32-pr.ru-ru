---
description: Отображает вкладку Общий доступ к папке на странице свойств указанной папки.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Функция Шовшарефолдеруи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346425"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="f254c-103">Функция Шовшарефолдеруи</span><span class="sxs-lookup"><span data-stu-id="f254c-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="f254c-104">Отображает вкладку **общий доступ к папке** на странице свойств указанной папки.</span><span class="sxs-lookup"><span data-stu-id="f254c-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="f254c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f254c-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="f254c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f254c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f254c-107">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f254c-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f254c-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="f254c-108">Type: **HWND**</span></span>

<span data-ttu-id="f254c-109">Маркер родительского окна для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f254c-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="f254c-110">*псзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f254c-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f254c-111">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="f254c-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="f254c-112">Указатель на строку, указывающую путь к папке, в которой отображается вкладка **совместного доступа к папке** .</span><span class="sxs-lookup"><span data-stu-id="f254c-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f254c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f254c-113">Return value</span></span>

<span data-ttu-id="f254c-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f254c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f254c-115">Эта функция всегда возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f254c-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f254c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f254c-116">Remarks</span></span>

<span data-ttu-id="f254c-117">Эта функция не имеет связанного LIB файла.</span><span class="sxs-lookup"><span data-stu-id="f254c-117">This function has no associated .lib file.</span></span> <span data-ttu-id="f254c-118">Для его использования необходимо использовать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f254c-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f254c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f254c-119">Requirements</span></span>



| <span data-ttu-id="f254c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f254c-120">Requirement</span></span> | <span data-ttu-id="f254c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f254c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f254c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f254c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f254c-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f254c-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f254c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f254c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f254c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f254c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f254c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f254c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f254c-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f254c-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="f254c-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f254c-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f254c-129">**Шовшарефолдеруив** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="f254c-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="f254c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f254c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f254c-131">**каншарефолдерв**</span><span class="sxs-lookup"><span data-stu-id="f254c-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
