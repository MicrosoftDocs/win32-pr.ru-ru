---
description: Метод Акцептпаренталлевелчанже принимает или отклоняет новый временный родительский уровень управления.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Метод Акцептпаренталлевелчанже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4742622ce9a2c65cdce660a8bae7fab6f84171d6bd61cdf88475c2bcd788c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873594"
---
# <a name="acceptparentallevelchange-method"></a>Метод Акцептпаренталлевелчанже

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

Метод Акцептпаренталлевелчанже принимает или отклоняет новый временный родительский уровень управления.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*бакцепт*
</dt> <dd>

Указывает новый родительский уровень в качестве логического значения.



| Значение | Описание                               |
|-------|-------------------------------------------|
| Да  | Примите новый уровень родительского управления. |
| false | Отклонить новый уровень родительского управления. |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Вызовите этот метод в ответ на \_ \_ \_ \_ уведомление о событии изменения родительского уровня EC, чтобы указать, должен ли навигатор DVD воспроизводить содержимое с новым родительским уровнем, или ветвь, где диск указывает, отклоняется ли новый уровень.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Применение уровней родительского управления](enforcing-parental-management-levels.md)
</dt> <dt>

[**жетплайерпаренталкаунтри**](getplayerparentalcountry-method.md)
</dt> <dt>

[**жетплайерпаренталлевел**](getplayerparentallevel-method.md)
</dt> <dt>

[**жеттитлепаренталлевелс**](gettitleparentallevels-method.md)
</dt> <dt>

[**нотифипаренталлевелчанже**](notifyparentallevelchange-method.md)
</dt> <dt>

[**селектпаренталкаунтри**](selectparentalcountry-method.md)
</dt> <dt>

[**селектпаренталлевел**](selectparentallevel-method.md)
</dt> </dl>

 

 



