---
title: Требования к датчикам для защиты биометрических информации
description: Требования к датчикам для защиты биометрических информации
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681650"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="7899e-103">Требования к датчикам для защиты биометрических информации</span><span class="sxs-lookup"><span data-stu-id="7899e-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="7899e-104">Корпорация Майкрософт использует доверенный платформенный модуль (TPM) (TPM) 2,0, чтобы убедиться, что на соответствующем оборудовании (до и включая вредоносные программы уровня ядра) не удается создать допустимую биометрическую проверку подлинности, если биометрия пользователя не были предоставлены во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7899e-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="7899e-105">Для этого мы используем авторизации на основе сеанса доверенного платформенного модуля (TPM 2,0) и датчик, выполняющий извлечение и сопоставление функций, в доверенной среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="7899e-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="7899e-106">В первый раз биометрическая платформа Windows видит защищенный датчик (как указано в функции безопасного датчика), он подготавливает секретный ключ, который является общим для защищенного биометрического датчика и доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="7899e-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="7899e-107">Этот секрет никогда не предоставляется операционной системе и уникален для каждого датчика.</span><span class="sxs-lookup"><span data-stu-id="7899e-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="7899e-108">Чтобы выполнить проверку подлинности, биометрическая платформа Windows открывает сеанс с доверенным платформенным модулем и получает nonce.</span><span class="sxs-lookup"><span data-stu-id="7899e-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="7899e-109">Элемент nonce передается в безопасный датчик в рамках операции безопасного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7899e-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="7899e-110">Датчик выполняет сопоставление в доверенной среде выполнения и при успешном выполнении вычисляет код HMAC для этого элемента и идентификатор пользователя, который был идентифицирован.</span><span class="sxs-lookup"><span data-stu-id="7899e-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="7899e-111">Этот код HMAC может использоваться биометрическая платформа Windows для выполнения криптографических операций в доверенном платформенном модуле для пользователя, который был идентифицирован.</span><span class="sxs-lookup"><span data-stu-id="7899e-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="7899e-112">Срок действия HMAC кратковременно истекает через несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="7899e-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="7899e-113">При использовании этого протокола после первоначальной подготовки в ОС не содержатся конфиденциальные данные.</span><span class="sxs-lookup"><span data-stu-id="7899e-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="7899e-114">Секретные данные удерживаются доверенным платформенным модулем и защищенным датчиком, а единственное, что предоставляется во время проверки подлинности, — это кратковременный HMAC.</span><span class="sxs-lookup"><span data-stu-id="7899e-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="7899e-115">Возможности безопасного датчика</span><span class="sxs-lookup"><span data-stu-id="7899e-115">Secure sensor capability</span></span>

<span data-ttu-id="7899e-116">Датчик ВИНБИО \_ возможностей \_ защищенного \_ датчика должен сообщать от датчика, если он поддерживает новые методы адаптера подсистемы в версии v 4,0 интерфейса адаптера подсистемы.</span><span class="sxs-lookup"><span data-stu-id="7899e-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="7899e-117">Чтобы убедиться, что датчик является безопасным датчиком, он должен соответствовать следующим требованиям:</span><span class="sxs-lookup"><span data-stu-id="7899e-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="7899e-118">Механизм сопоставления датчика должен быть изолирован от обычной ОС (например, с помощью доверенной среды выполнения).</span><span class="sxs-lookup"><span data-stu-id="7899e-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="7899e-119">Датчик должен поддерживать безопасный ввод образцов для изолированного механизма сопоставления; содержимое примеров никогда не должно предоставляться обычной ОС.</span><span class="sxs-lookup"><span data-stu-id="7899e-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="7899e-120">Механизм сопоставления должен поддерживать защищенный выпуск учетных данных, реализуя новые методы V4, описанные ниже.</span><span class="sxs-lookup"><span data-stu-id="7899e-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="7899e-121">Датчик должен поддерживать Обнаружение атак на презентацию.</span><span class="sxs-lookup"><span data-stu-id="7899e-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="7899e-122">\_ \_ Значение безопасного датчика возможностей винбио \_ содержится в структуре [**\_ возможностей винбио**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) .</span><span class="sxs-lookup"><span data-stu-id="7899e-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="7899e-123">Ниже приведен пример того, как определить его.</span><span class="sxs-lookup"><span data-stu-id="7899e-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="7899e-124">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7899e-124">Error Codes</span></span>


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="7899e-125">Интерфейс адаптера v 4,0</span><span class="sxs-lookup"><span data-stu-id="7899e-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="7899e-126">Версия интерфейса адаптера процессора была увеличена до 4,0.</span><span class="sxs-lookup"><span data-stu-id="7899e-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="7899e-127">Дополнительные функции в новом интерфейсе позволяют датчику участвовать в TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="7899e-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="7899e-128">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="7899e-128">They are:</span></span>

-   [<span data-ttu-id="7899e-129">**енгинеадаптеркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="7899e-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="7899e-130">**енгинеадаптеридентифифеатуресетсекуре**</span><span class="sxs-lookup"><span data-stu-id="7899e-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a><span data-ttu-id="7899e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7899e-131">Requirements</span></span>

<span data-ttu-id="7899e-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7899e-132">Windows 10</span></span>

 

 