---
title: Тфгуидатом (Мсктф. h)
description: Тип данных Тфгуидатом определяет идентификатор GUID в TSF. Тфгуидатом получается путем вызова Итфкатегоримгр Регистергуид.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- тфгуидатом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135062"
---
# <a name="tfguidatom"></a>тфгуидатом

Тип данных **тфгуидатом** определяет **идентификатор GUID** в TSF. **Тфгуидатом** получается путем вызова [**Итфкатегоримгр:: регистергуид**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a>Комментарии

Значение **тфгуидатом** допустимо только в пределах процесса, из которого вызывается **Итфкатегоримгр:: регистергуид** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                      |
| Header<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Итфкатегоримгр:: a GUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[**Итфкатегоримгр:: Исекуалтфгуидатом**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[**Итфкатегоримгр:: Регистергуид**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





