---
description: Загружает файл ресурсов AppHelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Функция Сдбопенапфелпресаурцефиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423345"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="9c57a-103">Функция Сдбопенапфелпресаурцефиле</span><span class="sxs-lookup"><span data-stu-id="9c57a-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="9c57a-104">Загружает файл ресурсов AppHelp.</span><span class="sxs-lookup"><span data-stu-id="9c57a-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c57a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c57a-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="9c57a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c57a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c57a-107">*пвсзакресаурцефиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9c57a-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c57a-108">Путь к файлу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c57a-108">The path to the resource file.</span></span> <span data-ttu-id="9c57a-109">Если этот параметр имеет **значение NULL**, то открывается Локальная библиотека ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c57a-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c57a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c57a-110">Return value</span></span>

<span data-ttu-id="9c57a-111">Функция возвращает маркер в открытый файл ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c57a-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c57a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9c57a-112">Requirements</span></span>



| <span data-ttu-id="9c57a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9c57a-113">Requirement</span></span> | <span data-ttu-id="9c57a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9c57a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c57a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c57a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9c57a-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c57a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9c57a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c57a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9c57a-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c57a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9c57a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9c57a-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c57a-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c57a-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




