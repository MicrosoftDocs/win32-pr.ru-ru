---
title: Тфедиткукие (Мсктф. h)
description: Тип данных Тфедиткукие определяет сеанс изменения, который имеет блокировку.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- тфедиткукие
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa397354ea7aa8addca4008d321162a99073345efc0761b65687f704a573ef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874082"
---
# <a name="tfeditcookie"></a>тфедиткукие

Тип данных **тфедиткукие** определяет сеанс изменения, который имеет блокировку.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Remarks

Тип данных **тфедиткукие** предоставляется диспетчером TSF и используется клиентом (приложением или службой текстового ввода) для обнаружения сеанса изменения с блокировкой только для чтения или для чтения и записи в различных методах.

Значение **тфедиткукие** получается одним из следующих способов.

-   Клиент вызывает [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).
-   Диспетчер TSF вызывает метод Client [итфедитсессион::D оедитсессион](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .
-   Диспетчер TSF вызывает метод [итфкомпоситионсинк:: онкомпоситионтерминатед](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) клиента.
-   Диспетчер TSF вызывает метод [итфклеанупконтекстсинк:: онклеанупконтекст](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) клиента.
-   Диспетчер TSF вызывает метод [итфтекстедитсинк:: онендедит](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) клиента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional приложения \[ UWP для классических приложений \|\]<br/>                    |
| Минимальная версия сервера<br/> | \[приложения UWP для классических приложений Windows 2000 \|\]<br/>                          |
| Распространяемые компоненты<br/>          | TSF 1,0 на Windows 2000 Professional<br/>                                      |
| Заголовок<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Итфклеанупконтекстсинк:: Онклеанупконтекст**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**Итфкомпоситионсинк:: Онкомпоситионтерминатед**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr:: CreateContext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**Итфедитсессион::D Оедитсессион**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**Итфтекстедитсинк:: Онендедит**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





