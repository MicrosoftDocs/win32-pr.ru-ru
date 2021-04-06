---
description: Записывает двоичные данные из указанного файла в указанную базу данных.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: Функция Сдбвритебинаритагфромфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990467"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="ab0c8-103">Функция Сдбвритебинаритагфромфиле</span><span class="sxs-lookup"><span data-stu-id="ab0c8-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="ab0c8-104">Записывает двоичные данные из указанного файла в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab0c8-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="ab0c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab0c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab0c8-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="ab0c8-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0c8-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ab0c8-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab0c8-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0c8-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-110">The TAG for the entry.</span></span> <span data-ttu-id="ab0c8-111">Этот тег должен иметь тип **\_ \_ binary типа Tag**.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="ab0c8-112">*пвсзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab0c8-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0c8-113">Путь к файлу, содержащему данные.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-113">The path to the file that contains the data.</span></span> <span data-ttu-id="ab0c8-114">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab0c8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab0c8-115">Return value</span></span>

<span data-ttu-id="ab0c8-116">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0c8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ab0c8-117">Requirements</span></span>



| <span data-ttu-id="ab0c8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ab0c8-118">Requirement</span></span> | <span data-ttu-id="ab0c8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ab0c8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0c8-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab0c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0c8-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab0c8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab0c8-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab0c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0c8-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab0c8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ab0c8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ab0c8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab0c8-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab0c8-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab0c8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab0c8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0c8-127">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="ab0c8-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 




