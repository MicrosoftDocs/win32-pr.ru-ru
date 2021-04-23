---
description: Используется поставщиком служб шифрования (CSP) для получения маркера окна, который CSP должен использовать в качестве родительского или владельца любого отображаемого пользовательского интерфейса.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: Указатель функции CRYPT_RETURN_HWND (Кспдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664407"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="d95c8-103">\_Функция шифрования возвращает \_ указатель функции HWND</span><span class="sxs-lookup"><span data-stu-id="d95c8-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="d95c8-104">Функция обратного вызова **функретурнхвнд** используется [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для получения маркера окна, который CSP должен использовать в качестве родительского или владельца любого отображаемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d95c8-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d95c8-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="d95c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d95c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95c8-107">*ФВНД* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d95c8-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d95c8-108">Адрес переменной **HWND** , которая получает дескриптор родительского окна.</span><span class="sxs-lookup"><span data-stu-id="d95c8-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95c8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d95c8-109">Return value</span></span>

<span data-ttu-id="d95c8-110">Этот указатель функции не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d95c8-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95c8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d95c8-111">Requirements</span></span>



| <span data-ttu-id="d95c8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d95c8-112">Requirement</span></span> | <span data-ttu-id="d95c8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d95c8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d95c8-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d95c8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d95c8-115">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d95c8-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d95c8-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d95c8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d95c8-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d95c8-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d95c8-118">Header</span><span class="sxs-lookup"><span data-stu-id="d95c8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d95c8-119"><dt>Кспдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d95c8-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d95c8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d95c8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95c8-121">**кпаккуиреконтекст**</span><span class="sxs-lookup"><span data-stu-id="d95c8-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="d95c8-122">**втаблепровструк**</span><span class="sxs-lookup"><span data-stu-id="d95c8-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
