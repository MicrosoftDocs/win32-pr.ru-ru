---
description: Отображает диалоговое окно, позволяющее пользователю выбрать сертификат.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Функция CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 8f015796671990491407d91cbd51761816c5434b
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925695"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="efd60-103">Функция CryptUIDlgSelectCertificate</span><span class="sxs-lookup"><span data-stu-id="efd60-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="efd60-104">Функция **криптуидлгселектцертификате** отображает диалоговое окно, позволяющее пользователю выбрать сертификат.</span><span class="sxs-lookup"><span data-stu-id="efd60-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efd60-105">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a><span data-ttu-id="efd60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efd60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd60-107">*ПКСК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efd60-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efd60-108">Указатель на структуру структуры [**динамической компоновки Cryptui \_ селектцертификате \_**](cryptui-selectcertificate-struct.md) , которая содержит сведения о диалоговом окне для вывода.</span><span class="sxs-lookup"><span data-stu-id="efd60-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd60-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efd60-109">Return value</span></span>

<span data-ttu-id="efd60-110">Указатель на структуру [**\_ контекста сертификата**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) , представляющую сертификат, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="efd60-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="efd60-111">После завершения использования этого сертификата необходимо передать этот указатель функции [**цертфрицертификатеконтекст**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) , чтобы уменьшить число ссылок контекста сертификата.</span><span class="sxs-lookup"><span data-stu-id="efd60-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="efd60-112">Если элемент **dwFlags** структуры *ПКСК* не содержит флаг **динамической компоновки Cryptui \_ Селектцерт \_ SELECT** , возвращаемое значение **null** означает, что пользователь закрыл диалоговое окно, не выбирая сертификат.</span><span class="sxs-lookup"><span data-stu-id="efd60-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="efd60-113">Если элемент **dwFlags** структуры *ПКСК* содержит флаг **динамической компоновки Cryptui \_ селектцерт \_ SELECT** , эта функция всегда возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="efd60-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="efd60-114">Выбранные сертификаты будут содержаться в хранилище сертификатов, представленном членом **хселектедцертсторе** *ПКСК*.</span><span class="sxs-lookup"><span data-stu-id="efd60-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="efd60-115">Если число сертификатов в хранилище одинаково до и после вызова **криптуидлгселектцертификате**, пользователь закрыл диалоговое окно, не выбирая сертификаты.</span><span class="sxs-lookup"><span data-stu-id="efd60-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="efd60-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efd60-116">Remarks</span></span>

<span data-ttu-id="efd60-117">Если элемент **dwFlags** структуры [**\_ \_ структуры динамической компоновки Cryptui селектцертификате**](cryptui-selectcertificate-struct.md) имеет значение **динамической компоновки Cryptui \_ селектцерт \_ Legacy**, то отображается диалоговое окно прежних версий.</span><span class="sxs-lookup"><span data-stu-id="efd60-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="efd60-118">В противном случае отображается диалоговое окно выбора текущего сертификата.</span><span class="sxs-lookup"><span data-stu-id="efd60-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="efd60-119">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="efd60-119">Requirements</span></span>



| <span data-ttu-id="efd60-120">Требование</span><span class="sxs-lookup"><span data-stu-id="efd60-120">Requirement</span></span> | <span data-ttu-id="efd60-121">Значение</span><span class="sxs-lookup"><span data-stu-id="efd60-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efd60-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efd60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="efd60-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="efd60-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="efd60-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efd60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="efd60-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efd60-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="efd60-126">Дата окончания поддержки</span><span class="sxs-lookup"><span data-stu-id="efd60-126">End of support</span></span><br/> | <span data-ttu-id="efd60-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="efd60-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="efd60-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="efd60-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="efd60-129"><dt>Динамической компоновки Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efd60-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="efd60-130">DLL</span><span class="sxs-lookup"><span data-stu-id="efd60-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efd60-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efd60-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="efd60-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="efd60-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="efd60-133">**Криптуидлгселектцертификатев** (Юникод) и **криптуидлгселектцертификатеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="efd60-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efd60-134">См. также</span><span class="sxs-lookup"><span data-stu-id="efd60-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd60-135">**\_Структура СЕЛЕКТЦЕРТИФИКАТЕ \_ динамической компоновки Cryptui**</span><span class="sxs-lookup"><span data-stu-id="efd60-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>






