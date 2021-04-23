---
description: Запрос на отправку путей к символам отладки локальному (не удаленному) подсистеме.
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исимболсеттингс:: Упдатесимболсеттингс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710585"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span data-ttu-id="af25b-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>Метод Исимболсеттингс:: Упдатесимболсеттингс</span><span class="sxs-lookup"><span data-stu-id="af25b-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings::UpdateSymbolSettings method</span></span>

<span data-ttu-id="af25b-104">Запрос на отправку путей к символам отладки локальному (не удаленному) подсистеме.</span><span class="sxs-lookup"><span data-stu-id="af25b-104">A request to send debug symbol paths to the local (non-remote) engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="af25b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af25b-105">Syntax</span></span>


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a><span data-ttu-id="af25b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af25b-106">Parameters</span></span>

<span data-ttu-id="af25b-107">*симболсерверинфо* </span><span class="sxs-lookup"><span data-stu-id="af25b-107">*symbolServerInfo* </span></span>  
<span data-ttu-id="af25b-108">Сведения о пути к серверу символов отладки.</span><span class="sxs-lookup"><span data-stu-id="af25b-108">Debug symbol server path information.</span></span>

## <a name="return-value"></a><span data-ttu-id="af25b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af25b-109">Return value</span></span>

<span data-ttu-id="af25b-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="af25b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af25b-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af25b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af25b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="af25b-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="af25b-113">Header</span><span class="sxs-lookup"><span data-stu-id="af25b-113">Header</span></span></p></td><td><span data-ttu-id="af25b-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="af25b-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="af25b-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="af25b-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="af25b-116">**исимболсеттингс**</span><span class="sxs-lookup"><span data-stu-id="af25b-116">**ISymbolSettings**</span></span>](/windows/desktop/direct3dtools/isymbolsettings)

 

 
