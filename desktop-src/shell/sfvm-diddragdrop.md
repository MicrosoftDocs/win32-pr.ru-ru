---
description: СФВМ \_ диддрагдроп может быть изменен или недоступен.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Сообщение SFVM_DIDDRAGDROP (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997826"
---
# <a name="sfvm_diddragdrop-message"></a>\_Сообщение сфвм диддрагдроп

\[**Сфвм \_ ДИДДРАГДРОП** доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Уведомляет функцию обратного вызова о начале операции перетаскивания. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двеффект* \[ окне\]
</dt> <dd>

Описатель эффекты перетаскивания из перечисления [**дропеффект**](../com/dropeffect-constants.md) . Это достигается путем вызова [**шдодрагдроп**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).

</dd> <dt>

*Пидо* \[ окне\]
</dt> <dd>

Указатель на экземпляр [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
