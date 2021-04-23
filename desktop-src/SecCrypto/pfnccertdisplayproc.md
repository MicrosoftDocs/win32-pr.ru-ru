---
description: Определяемая пользователем функция обратного вызова, позволяющая вызывающему объекту функции Криптуидлгселектцертификате управлять отображением сертификатов, которые пользователь выбирает для просмотра.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Функция обратного вызова ПФНКЦЕРТДИСПЛАЙПРОК
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080847"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="55399-103">Функция обратного вызова ПФНКЦЕРТДИСПЛАЙПРОК</span><span class="sxs-lookup"><span data-stu-id="55399-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="55399-104">Функция **пфнкцертдисплайпрок** — это определяемая пользователем функция обратного вызова, которая позволяет вызывающей стороне функции [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md) управлять отображением сертификатов, которые пользователь выбирает для просмотра.</span><span class="sxs-lookup"><span data-stu-id="55399-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="55399-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55399-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="55399-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55399-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55399-107">*пцертконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55399-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55399-108">Указатель на структуру [**\_ контекста сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) , представляющую сертификат для вывода.</span><span class="sxs-lookup"><span data-stu-id="55399-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="55399-109">*хвндселцертдлг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55399-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55399-110">Описатель диалогового окна, из которого был выбран сертификат для просмотра.</span><span class="sxs-lookup"><span data-stu-id="55399-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="55399-111">*пвкаллбаккдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55399-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55399-112">Дополнительные данные, используемые функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="55399-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55399-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55399-113">Return value</span></span>

<span data-ttu-id="55399-114">Эта функция возвращает **значение true** , чтобы указать, что она обрабатывает отображение сертификата и что диалоговое окно не должно отображать сертификат.</span><span class="sxs-lookup"><span data-stu-id="55399-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="55399-115">Если эта функция возвращает **значение false**, то в диалоговом окне отображается сертификат.</span><span class="sxs-lookup"><span data-stu-id="55399-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="55399-116">Требования</span><span class="sxs-lookup"><span data-stu-id="55399-116">Requirements</span></span>



| <span data-ttu-id="55399-117">Требование</span><span class="sxs-lookup"><span data-stu-id="55399-117">Requirement</span></span> | <span data-ttu-id="55399-118">Значение</span><span class="sxs-lookup"><span data-stu-id="55399-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55399-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55399-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55399-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55399-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="55399-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55399-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55399-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55399-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




