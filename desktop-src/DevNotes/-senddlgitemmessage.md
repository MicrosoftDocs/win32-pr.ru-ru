---
description: Отправляет сообщение указанному элементу управления в диалоговом окне.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: Функция _SendDlgItemMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657015"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="ebc0e-103">\_Функция Сенддлгитеммессаже</span><span class="sxs-lookup"><span data-stu-id="ebc0e-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="ebc0e-104">\[Эта функция является оболочкой для функции **сенддлгитеммессаже** .</span><span class="sxs-lookup"><span data-stu-id="ebc0e-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="ebc0e-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="ebc0e-106">Приложения должны вызывать **сенддлгитеммессаже** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="ebc0e-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="ebc0e-107">Отправляет сообщение указанному элементу управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="ebc0e-108">См. [**сенддлгитеммессаже**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span><span class="sxs-lookup"><span data-stu-id="ebc0e-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc0e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebc0e-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="ebc0e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebc0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc0e-111">*...*</span><span class="sxs-lookup"><span data-stu-id="ebc0e-111">*...*</span></span> 
<span data-ttu-id="ebc0e-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ebc0e-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ebc0e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ebc0e-113">Requirements</span></span>



| <span data-ttu-id="ebc0e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ebc0e-114">Requirement</span></span> | <span data-ttu-id="ebc0e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ebc0e-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc0e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ebc0e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ebc0e-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebc0e-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc0e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebc0e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc0e-119">**сенддлгитеммессаже**</span><span class="sxs-lookup"><span data-stu-id="ebc0e-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
