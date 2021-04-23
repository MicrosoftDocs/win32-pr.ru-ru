---
Description: Извлекает данные из базы данных сведений о AppHelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Функция Сдбреадапфелпдетаилсдата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988589"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="08b7f-103">Функция Сдбреадапфелпдетаилсдата</span><span class="sxs-lookup"><span data-stu-id="08b7f-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="08b7f-104">Извлекает данные из базы данных сведений о AppHelp.</span><span class="sxs-lookup"><span data-stu-id="08b7f-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08b7f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="08b7f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08b7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b7f-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="08b7f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b7f-108">Описатель для базы данных AppHelp Details, AppHelp. sdb.</span><span class="sxs-lookup"><span data-stu-id="08b7f-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="08b7f-109">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="08b7f-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08b7f-110">Структура [**\_ данных APPHELP**](apphelp-data.md) .</span><span class="sxs-lookup"><span data-stu-id="08b7f-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b7f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08b7f-111">Return value</span></span>

<span data-ttu-id="08b7f-112">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="08b7f-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b7f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="08b7f-113">Requirements</span></span>



| <span data-ttu-id="08b7f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="08b7f-114">Requirement</span></span> | <span data-ttu-id="08b7f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="08b7f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08b7f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08b7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08b7f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08b7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08b7f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08b7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08b7f-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08b7f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="08b7f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="08b7f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b7f-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b7f-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




