---
description: Shell. Шовбровсербар-метод — отображает панель браузера.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Метод Shell. Шовбровсербар (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083732"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="79d85-103">Shell. Шовбровсербар, метод</span><span class="sxs-lookup"><span data-stu-id="79d85-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="79d85-104">Отображает панель браузера.</span><span class="sxs-lookup"><span data-stu-id="79d85-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d85-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79d85-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="79d85-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79d85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d85-107">*склсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79d85-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d85-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="79d85-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="79d85-109">**Строка** , содержащая форму строки CLSID отображаемой панели браузера.</span><span class="sxs-lookup"><span data-stu-id="79d85-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="79d85-110">Объект должен быть зарегистрирован в качестве объекта панели обозревателя с \_ категорией компонента CATID инфобанд.</span><span class="sxs-lookup"><span data-stu-id="79d85-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="79d85-111">Дополнительные сведения см. в разделе [Создание настраиваемых панелей обозревателя, панелей инструментов и полос рабочего стола](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="79d85-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="79d85-112">*вшов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79d85-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d85-113">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="79d85-113">Type: **Variant**</span></span>

<span data-ttu-id="79d85-114">Задайте значение **true** , чтобы отобразить панель браузера, или **значение false** , чтобы скрыть ее.</span><span class="sxs-lookup"><span data-stu-id="79d85-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d85-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79d85-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="79d85-116">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="79d85-116">JScript</span></span>

<span data-ttu-id="79d85-117">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="79d85-117">Type: **Variant\***</span></span>

<span data-ttu-id="79d85-118">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="79d85-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="79d85-119">VB</span><span class="sxs-lookup"><span data-stu-id="79d85-119">VB</span></span>

<span data-ttu-id="79d85-120">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="79d85-120">Type: **Variant\***</span></span>

<span data-ttu-id="79d85-121">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="79d85-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="79d85-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="79d85-122">Remarks</span></span>

<span data-ttu-id="79d85-123">Можно отобразить одну из стандартных панелей обозревателя, задав для параметра *склсид* значение CLSID этой панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="79d85-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="79d85-124">Ниже перечислены стандартные панели обозревателя и их строки CLSID.</span><span class="sxs-lookup"><span data-stu-id="79d85-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="79d85-125">Панель обозревателя</span><span class="sxs-lookup"><span data-stu-id="79d85-125">Explorer Bar</span></span> | <span data-ttu-id="79d85-126">Строка CLSID</span><span class="sxs-lookup"><span data-stu-id="79d85-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="79d85-127">Избранное</span><span class="sxs-lookup"><span data-stu-id="79d85-127">Favorites</span></span>    | <span data-ttu-id="79d85-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="79d85-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="79d85-129">Папки</span><span class="sxs-lookup"><span data-stu-id="79d85-129">Folders</span></span>      | <span data-ttu-id="79d85-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="79d85-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="79d85-131">Журнал</span><span class="sxs-lookup"><span data-stu-id="79d85-131">History</span></span>      | <span data-ttu-id="79d85-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="79d85-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="79d85-133">Поиск</span><span class="sxs-lookup"><span data-stu-id="79d85-133">Search</span></span>       | <span data-ttu-id="79d85-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="79d85-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="79d85-135">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="79d85-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="79d85-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="79d85-136">Examples</span></span>

<span data-ttu-id="79d85-137">В следующих примерах показано использование **оболочки. шовбровсербар** для отображения панели браузера **избранного** .</span><span class="sxs-lookup"><span data-stu-id="79d85-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="79d85-138">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="79d85-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="79d85-139">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="79d85-139">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="79d85-140">Сценариев</span><span class="sxs-lookup"><span data-stu-id="79d85-140">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="79d85-141">Требования</span><span class="sxs-lookup"><span data-stu-id="79d85-141">Requirements</span></span>



| <span data-ttu-id="79d85-142">Требование</span><span class="sxs-lookup"><span data-stu-id="79d85-142">Requirement</span></span> | <span data-ttu-id="79d85-143">Значение</span><span class="sxs-lookup"><span data-stu-id="79d85-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d85-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79d85-144">Minimum supported client</span></span><br/> | <span data-ttu-id="79d85-145">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="79d85-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79d85-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79d85-146">Minimum supported server</span></span><br/> | <span data-ttu-id="79d85-147">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79d85-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="79d85-148">Header</span><span class="sxs-lookup"><span data-stu-id="79d85-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="79d85-149"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d85-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="79d85-150">IDL</span><span class="sxs-lookup"><span data-stu-id="79d85-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79d85-151"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79d85-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="79d85-152">DLL</span><span class="sxs-lookup"><span data-stu-id="79d85-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79d85-153"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="79d85-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
