---
description: Содержит указатели на функции обратного вызова, которые могут использоваться функциями поставщика служб шифрования (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Структура Втаблепровструк (Кспдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817633"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="fcae2-103">Структура Втаблепровструк</span><span class="sxs-lookup"><span data-stu-id="fcae2-103">VTableProvStruc structure</span></span>

<span data-ttu-id="fcae2-104">Структура **втаблепровструк** содержит указатели на функции обратного вызова, которые могут использоваться функциями [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="fcae2-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcae2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcae2-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="fcae2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="fcae2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fcae2-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="fcae2-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-108">Значение **типа DWORD** , указывающее версию структуры.</span><span class="sxs-lookup"><span data-stu-id="fcae2-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="fcae2-109">Используются три версии этой структуры.</span><span class="sxs-lookup"><span data-stu-id="fcae2-109">Three versions of this structure are used.</span></span> <span data-ttu-id="fcae2-110">Версии имеют номер 1, 2 и 3, а также определяют, какие члены структуры являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="fcae2-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="fcae2-111">Члены версии 1 действительны во всех системах, поддерживающих эту структуру.</span><span class="sxs-lookup"><span data-stu-id="fcae2-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="fcae2-112">Это член версии 1.</span><span class="sxs-lookup"><span data-stu-id="fcae2-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="fcae2-113">**функверифимаже**</span><span class="sxs-lookup"><span data-stu-id="fcae2-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-114">Адрес функции обратного вызова [**функверифимаже**](funcverifyimage.md) , которую CSP использует для проверки подписи любых библиотек DLL, которые будет загружать CSP.</span><span class="sxs-lookup"><span data-stu-id="fcae2-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="fcae2-115">Все вспомогательные библиотеки DLL, в которые CSP вызывает вызовы функций, должны быть подписаны аналогичным образом (и с тем же ключом), что и первичная библиотека CSP.</span><span class="sxs-lookup"><span data-stu-id="fcae2-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="fcae2-116">Чтобы обеспечить эту сигнатуру, вспомогательные библиотеки DLL должны динамически загружаться с помощью функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="fcae2-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="fcae2-117">Но перед загрузкой библиотеки DLL необходимо проверить подпись библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="fcae2-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="fcae2-118">CSP выполняет эту проверку, вызывая функцию **функверифимаже** , как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="fcae2-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="fcae2-119">Этот указатель функции можно хранить и использовать до тех пор, пока не будет освобожден контекст CSP.</span><span class="sxs-lookup"><span data-stu-id="fcae2-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="fcae2-120">Это член версии 1.</span><span class="sxs-lookup"><span data-stu-id="fcae2-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="fcae2-121">**функретурнхвнд**</span><span class="sxs-lookup"><span data-stu-id="fcae2-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-122">Адрес функции обратного вызова [**функретурнхвнд**](funcreturnhwnd.md) , возвращающей маркер окна, который CSP должен использовать в качестве родителя или владельца любого отображаемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fcae2-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="fcae2-123">Поставщики CSP, которые не обмениваются данными напрямую с пользователем и CSP, использующие выделенное оборудование для этой цели, могут игнорировать эту запись.</span><span class="sxs-lookup"><span data-stu-id="fcae2-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="fcae2-124">По умолчанию дескриптор окна равен нулю, но приложение может задать другое значение с помощью функции [**криптсетпровпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) , чтобы задать свойство **\_ \_ HWND клиента PP** .</span><span class="sxs-lookup"><span data-stu-id="fcae2-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="fcae2-125">Этот указатель функции можно хранить и использовать до тех пор, пока не будет освобожден контекст CSP.</span><span class="sxs-lookup"><span data-stu-id="fcae2-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="fcae2-126">Это член версии 1.</span><span class="sxs-lookup"><span data-stu-id="fcae2-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="fcae2-127">**двпровтипе**</span><span class="sxs-lookup"><span data-stu-id="fcae2-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-128">Значение типа **DWORD** , указывающее тип получаемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="fcae2-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="fcae2-129">Следующие [*типы поставщиков*](../secgloss/p-gly.md) являются стандартными и подробно рассматриваются в разделе [взаимодействие с CSP](https://www.bing.com/search?q=CSP+Interoperability):</span><span class="sxs-lookup"><span data-stu-id="fcae2-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="fcae2-130">PROV \_ RSA \_ Full</span><span class="sxs-lookup"><span data-stu-id="fcae2-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="fcae2-131">PROV \_ RSA \_ SIG</span><span class="sxs-lookup"><span data-stu-id="fcae2-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="fcae2-132">PROV \_ DSS</span><span class="sxs-lookup"><span data-stu-id="fcae2-132">PROV\_DSS</span></span>
-   <span data-ttu-id="fcae2-133">PROV \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="fcae2-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="fcae2-134">PROV \_ MS \_ Exchange</span><span class="sxs-lookup"><span data-stu-id="fcae2-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="fcae2-135">Это член версии 2.</span><span class="sxs-lookup"><span data-stu-id="fcae2-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="fcae2-136">**пбконтекстинфо**</span><span class="sxs-lookup"><span data-stu-id="fcae2-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-137">Указатель на массив сведений о контексте.</span><span class="sxs-lookup"><span data-stu-id="fcae2-137">A pointer to an array of context information.</span></span> <span data-ttu-id="fcae2-138">Члены **пбконтекстинфо** и **кбконтекстинфо** вместе определяют набор данных, используемый при вызове функции [**кпсетпровпарам**](https://www.bing.com/search?q=**CPSetProvParam**) с \_ \_ набором сведений контекста PP.</span><span class="sxs-lookup"><span data-stu-id="fcae2-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="fcae2-139">Это член версии 2.</span><span class="sxs-lookup"><span data-stu-id="fcae2-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="fcae2-140">**кбконтекстинфо**</span><span class="sxs-lookup"><span data-stu-id="fcae2-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-141">Значение **типа DWORD** , указывающее количество элементов в массиве **пбконтекстинфо** .</span><span class="sxs-lookup"><span data-stu-id="fcae2-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="fcae2-142">Это член версии 2.</span><span class="sxs-lookup"><span data-stu-id="fcae2-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="fcae2-143">**псзпровнаме**</span><span class="sxs-lookup"><span data-stu-id="fcae2-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="fcae2-144">Строка, содержащая имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="fcae2-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="fcae2-145">Это член версии 3.</span><span class="sxs-lookup"><span data-stu-id="fcae2-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcae2-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcae2-146">Remarks</span></span>

<span data-ttu-id="fcae2-147">Указатели в структуре **втаблепровструк** доступны только в функции [**кпаккуиреконтекст**](https://www.bing.com/search?q=**CPAcquireContext**) .</span><span class="sxs-lookup"><span data-stu-id="fcae2-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="fcae2-148">Если элементы структуры необходимы после завершения вызова **кпаккуиреконтекст** , то CSP должны сделать копии необходимых элементов структуры.</span><span class="sxs-lookup"><span data-stu-id="fcae2-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="fcae2-149">Указатели функций в этой структуре можно хранить и использовать до тех пор, пока не будет освобожден контекст CSP.</span><span class="sxs-lookup"><span data-stu-id="fcae2-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcae2-150">Требования</span><span class="sxs-lookup"><span data-stu-id="fcae2-150">Requirements</span></span>



| <span data-ttu-id="fcae2-151">Требование</span><span class="sxs-lookup"><span data-stu-id="fcae2-151">Requirement</span></span> | <span data-ttu-id="fcae2-152">Значение</span><span class="sxs-lookup"><span data-stu-id="fcae2-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fcae2-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcae2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="fcae2-154">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fcae2-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcae2-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcae2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="fcae2-156">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcae2-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fcae2-157">Header</span><span class="sxs-lookup"><span data-stu-id="fcae2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcae2-158"><dt>Кспдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcae2-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="fcae2-159">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="fcae2-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fcae2-160">**Втаблепровструкв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="fcae2-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
