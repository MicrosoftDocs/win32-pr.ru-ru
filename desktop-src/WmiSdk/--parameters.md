---
description: Определяет входные и выходные параметры для методов.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Класс __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693160"
---
# <a name="__parameters-class"></a>\_\_Класс параметров

Системный класс **\_ \_ параметров** — это абстрактный класс, который определяет входные и выходные параметры для методов. Он также используется для передачи значений входных и выходных параметров между клиентом WMI и поставщиком метода.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Члены

Класс **\_ \_ параметров** не определяет никаких членов.

## <a name="remarks"></a>Комментарии

Чтобы определить метод в пользовательском классе, клиент WMI создает копию класса **\_ \_ Parameters** и добавляет свойство для каждого входного параметра в методе. Если метод содержит возвращаемое значение или выходные параметры, необходимо создать еще одну копию **\_ \_ параметров** . Если метод возвращает возвращаемое значение, клиент должен добавить свойство с именем **ReturnValue**. Затем поставщик метода сохраняет параметры метода с помощью вызова [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Чтобы вызвать метод, клиент вызывает следующую последовательность:

1.  [**Ивбемклассобжект::-Method**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) для получения копии класса **\_ \_ Parameters** , хранящегося в [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**Ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), а затем устанавливает по одному свойству для каждого входного параметра в метод.
3.  [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) или [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) для выполнения метода.

После завершения выполнения метода может возвращаться другой экземпляр класса **\_ \_ Parameters** , если метод имеет выходные параметры или возвращаемое значение.

-   Если метод был вызван с помощью [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), то экземпляр **\_ \_ параметров** возвращается в качестве выходного аргумента.
-   Если метод был вызван с помощью [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), то экземпляр **\_ \_ параметров** возвращается в качестве параметра [**ивбемобжектсинк::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices:: Ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

 




