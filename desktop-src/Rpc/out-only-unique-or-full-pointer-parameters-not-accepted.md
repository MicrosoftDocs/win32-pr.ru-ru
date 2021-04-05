---
title: Out-Only параметры уникального или полного указателя не приняты
description: Уникальные или полные указатели, т. е. которые не принимаются компилятором MIDL. Такие спецификации приводят к тому, что компилятор MIDL создает сообщение об ошибке.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533362"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="db128-104">Out-Only параметры уникального или полного указателя не приняты</span><span class="sxs-lookup"><span data-stu-id="db128-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="db128-105">\[КОМПИЛЯТОР MIDL не принимает уникальные или полные указатели [, которые являются](/windows/desktop/Midl/out-idl)недопустимыми \] .</span><span class="sxs-lookup"><span data-stu-id="db128-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="db128-106">Такие спецификации приводят к тому, что компилятор MIDL создает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="db128-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="db128-107">Автоматически созданная заглушка сервера должна выделить память для референт указателя, чтобы серверное приложение могла хранить данные в этой области памяти.</span><span class="sxs-lookup"><span data-stu-id="db128-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="db128-108">В соответствии с определением параметра, доступного только **\[ \] для использования,** сведения о параметре не передаются с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="db128-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="db128-109">В случае с уникальным указателем, который может принимать значение null, заглушка сервера не содержит достаточных сведений для правильного дублирования уникального указателя в адресном пространстве сервера, а заглушка не имеет никакой информации о том, должен ли указатель указывать на допустимый адрес или значение null.</span><span class="sxs-lookup"><span data-stu-id="db128-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="db128-110">Поэтому это сочетание не разрешено.</span><span class="sxs-lookup"><span data-stu-id="db128-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="db128-111">Указатели, а не "out", "Unique" и "out", "PTR", "a", "out", "Unique" или "in", "PTR" или \[  [](/windows/desktop/Midl/unique) \] \[  [](/windows/desktop/Midl/ptr) \] \[    \] \[    \] используют другой уровень косвенного обращения, например указатель ссылки, указывающий на допустимый уникальный или полный указатель.</span><span class="sxs-lookup"><span data-stu-id="db128-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 