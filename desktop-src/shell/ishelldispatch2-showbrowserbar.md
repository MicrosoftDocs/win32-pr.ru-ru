---
description: Отображает панель браузера.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: IShellDispatch2. Шовбровсербар, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984668"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="f95c6-103">IShellDispatch2. Шовбровсербар, метод</span><span class="sxs-lookup"><span data-stu-id="f95c6-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="f95c6-104">Отображает панель браузера.</span><span class="sxs-lookup"><span data-stu-id="f95c6-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f95c6-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="f95c6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f95c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95c6-107">*склсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f95c6-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f95c6-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f95c6-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f95c6-109">**Строка** , содержащая форму строки CLSID отображаемой панели браузера.</span><span class="sxs-lookup"><span data-stu-id="f95c6-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="f95c6-110">Объект должен быть зарегистрирован в качестве объекта панели обозревателя с \_ категорией компонента CATID инфобанд.</span><span class="sxs-lookup"><span data-stu-id="f95c6-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="f95c6-111">Дополнительные сведения см. в разделе [Создание настраиваемых панелей обозревателя, панелей инструментов и полос рабочего стола](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f95c6-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95c6-112">*вшов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f95c6-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f95c6-113">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="f95c6-113">Type: **Variant**</span></span>

<span data-ttu-id="f95c6-114">Задайте значение **true** , чтобы отобразить панель браузера, или **значение false** , чтобы скрыть ее.</span><span class="sxs-lookup"><span data-stu-id="f95c6-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95c6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f95c6-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f95c6-116">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="f95c6-116">JScript</span></span>

<span data-ttu-id="f95c6-117">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="f95c6-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="f95c6-118">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f95c6-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="f95c6-119">VB</span><span class="sxs-lookup"><span data-stu-id="f95c6-119">VB</span></span>

<span data-ttu-id="f95c6-120">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="f95c6-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="f95c6-121">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f95c6-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f95c6-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="f95c6-122">Remarks</span></span>

<span data-ttu-id="f95c6-123">Этот метод реализован и доступен через метод [**Shell. шовбровсербар**](./shell-showbrowserbar.md) .</span><span class="sxs-lookup"><span data-stu-id="f95c6-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="f95c6-124">Можно отобразить одну из стандартных панелей обозревателя, задав для параметра *склсид* значение CLSID этой панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="f95c6-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="f95c6-125">Ниже перечислены стандартные панели обозревателя и их строки CLSID.</span><span class="sxs-lookup"><span data-stu-id="f95c6-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="f95c6-126">Панель обозревателя</span><span class="sxs-lookup"><span data-stu-id="f95c6-126">Explorer Bar</span></span> | <span data-ttu-id="f95c6-127">Строка CLSID</span><span class="sxs-lookup"><span data-stu-id="f95c6-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="f95c6-128">Избранное</span><span class="sxs-lookup"><span data-stu-id="f95c6-128">Favorites</span></span>    | <span data-ttu-id="f95c6-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="f95c6-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="f95c6-130">Папки</span><span class="sxs-lookup"><span data-stu-id="f95c6-130">Folders</span></span>      | <span data-ttu-id="f95c6-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="f95c6-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="f95c6-132">Журнал</span><span class="sxs-lookup"><span data-stu-id="f95c6-132">History</span></span>      | <span data-ttu-id="f95c6-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="f95c6-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="f95c6-134">Найти</span><span class="sxs-lookup"><span data-stu-id="f95c6-134">Search</span></span>       | <span data-ttu-id="f95c6-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="f95c6-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="f95c6-136">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f95c6-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="f95c6-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="f95c6-137">Examples</span></span>

<span data-ttu-id="f95c6-138">В следующих примерах показано использование **шовбровсербар** для отображения панели браузера **избранного** .</span><span class="sxs-lookup"><span data-stu-id="f95c6-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="f95c6-139">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="f95c6-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="f95c6-140">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="f95c6-140">JScript:</span></span>


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



<span data-ttu-id="f95c6-141">Сценариев</span><span class="sxs-lookup"><span data-stu-id="f95c6-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f95c6-142">Требования</span><span class="sxs-lookup"><span data-stu-id="f95c6-142">Requirements</span></span>



| <span data-ttu-id="f95c6-143">Требование</span><span class="sxs-lookup"><span data-stu-id="f95c6-143">Requirement</span></span> | <span data-ttu-id="f95c6-144">Значение</span><span class="sxs-lookup"><span data-stu-id="f95c6-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f95c6-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f95c6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f95c6-146">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f95c6-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f95c6-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f95c6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f95c6-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f95c6-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f95c6-149">Header</span><span class="sxs-lookup"><span data-stu-id="f95c6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f95c6-150"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f95c6-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f95c6-151">IDL</span><span class="sxs-lookup"><span data-stu-id="f95c6-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f95c6-152"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f95c6-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f95c6-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f95c6-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f95c6-154"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f95c6-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
