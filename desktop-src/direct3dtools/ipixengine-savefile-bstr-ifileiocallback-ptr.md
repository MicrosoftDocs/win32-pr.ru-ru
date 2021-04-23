---
description: Сохраняет журнал графики в указанном расположении.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксенгине:: SaveFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538195"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="dbe09-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>Метод Ипиксенгине:: SaveFile</span><span class="sxs-lookup"><span data-stu-id="dbe09-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="dbe09-104">Сохраняет журнал графики в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="dbe09-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe09-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbe09-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="dbe09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbe09-106">Parameters</span></span>

<span data-ttu-id="dbe09-107">*Файлов* </span><span class="sxs-lookup"><span data-stu-id="dbe09-107">*FileName* </span></span>  
<span data-ttu-id="dbe09-108">Строка COM, содержащая путь к сохраненному журналу графики.</span><span class="sxs-lookup"><span data-stu-id="dbe09-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="dbe09-109">*пфилеиокаллбакк* </span><span class="sxs-lookup"><span data-stu-id="dbe09-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="dbe09-110">Адрес функтон, используемый для уведомления узла об ошибках ввода-вывода в файле при сохранении.</span><span class="sxs-lookup"><span data-stu-id="dbe09-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbe09-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbe09-111">Return value</span></span>

<span data-ttu-id="dbe09-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dbe09-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbe09-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbe09-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe09-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dbe09-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dbe09-115">Header</span><span class="sxs-lookup"><span data-stu-id="dbe09-115">Header</span></span></p></td><td><span data-ttu-id="dbe09-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="dbe09-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dbe09-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="dbe09-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dbe09-118">**ипиксенгине**</span><span class="sxs-lookup"><span data-stu-id="dbe09-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
