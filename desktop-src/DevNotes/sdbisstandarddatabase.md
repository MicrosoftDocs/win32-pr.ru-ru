---
description: Определяет, является ли указанная база данных одной из стандартных баз данных (Сисмаин, AppHelp, Дрвмаин или Мсимаин).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Функция Сдбисстандарддатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072341"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="0be51-103">Функция Сдбисстандарддатабасе</span><span class="sxs-lookup"><span data-stu-id="0be51-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="0be51-104">Определяет, является ли указанная база данных одной из стандартных баз данных (Сисмаин, AppHelp, Дрвмаин или Мсимаин).</span><span class="sxs-lookup"><span data-stu-id="0be51-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="0be51-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0be51-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="0be51-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0be51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be51-107">*Гуиддб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be51-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be51-108">Идентификатор GUID для базы данных.</span><span class="sxs-lookup"><span data-stu-id="0be51-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be51-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0be51-109">Return value</span></span>

<span data-ttu-id="0be51-110">Функция возвращает **значение true** , если идентификатор GUID представляет стандартную базу данных, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0be51-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be51-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0be51-111">Requirements</span></span>



| <span data-ttu-id="0be51-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0be51-112">Requirement</span></span> | <span data-ttu-id="0be51-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0be51-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0be51-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0be51-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0be51-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0be51-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0be51-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0be51-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0be51-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0be51-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0be51-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0be51-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0be51-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0be51-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




