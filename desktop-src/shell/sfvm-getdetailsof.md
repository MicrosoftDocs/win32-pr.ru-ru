---
description: СФВМ \_ жетдетаилсоф может быть изменен или недоступен.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Сообщение SFVM_GETDETAILSOF (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985769"
---
# <a name="sfvm_getdetailsof-message"></a>\_Сообщение сфвм жетдетаилсоф

\[**Сфвм \_ ЖЕТДЕТАИЛСОФ** доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Позволяет объекту обратного вызова предоставлять сведения для элемента в папке оболочки. Используйте только в случае, если вызов [**IShellFolder2:: жетдетаилсоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) завершается с ошибкой и отсутствует доступный для вызова метод [**Ишеллдетаилс:: жетдетаилсоф**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) . Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*иколумн* \[ окне\]
</dt> <dd>

Идентификатор столбца, начинающийся с нуля.

</dd> <dt>

*ПДИ* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**детаилсинфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) , заполненную запрошенной информацией.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
