(function() {
    const d = document.createElement("link").relList;
    if (d && d.supports && d.supports("modulepreload"))
        return;
    for (const m of document.querySelectorAll('link[rel="modulepreload"]'))
        f(m);
    new MutationObserver(m => {
        for (const g of m)
            if (g.type === "childList")
                for (const p of g.addedNodes)
                    p.tagName === "LINK" && p.rel === "modulepreload" && f(p)
    }
    ).observe(document, {
        childList: !0,
        subtree: !0
    });
    function o(m) {
        const g = {};
        return m.integrity && (g.integrity = m.integrity),
        m.referrerPolicy && (g.referrerPolicy = m.referrerPolicy),
        m.crossOrigin === "use-credentials" ? g.credentials = "include" : m.crossOrigin === "anonymous" ? g.credentials = "omit" : g.credentials = "same-origin",
        g
    }
    function f(m) {
        if (m.ep)
            return;
        m.ep = !0;
        const g = o(m);
        fetch(m.href, g)
    }
}
)();
function Sm(s) {
    return s && s.__esModule && Object.prototype.hasOwnProperty.call(s, "default") ? s.default : s
}
var Rs = {
    exports: {}
}
  , qn = {};
/**
 * @license React
 * react-jsx-runtime.production.js
 *
 * Copyright (c) Meta Platforms, Inc. and affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
var lm;
function dg() {
    if (lm)
        return qn;
    lm = 1;
    var s = Symbol.for("react.transitional.element")
      , d = Symbol.for("react.fragment");
    function o(f, m, g) {
        var p = null;
        if (g !== void 0 && (p = "" + g),
        m.key !== void 0 && (p = "" + m.key),
        "key"in m) {
            g = {};
            for (var T in m)
                T !== "key" && (g[T] = m[T])
        } else
            g = m;
        return m = g.ref,
        {
            $$typeof: s,
            type: f,
            key: p,
            ref: m !== void 0 ? m : null,
            props: g
        }
    }
    return qn.Fragment = d,
    qn.jsx = o,
    qn.jsxs = o,
    qn
}
var am;
function mg() {
    return am || (am = 1,
    Rs.exports = dg()),
    Rs.exports
}
var i = mg()
  , Us = {
    exports: {}
}
  , W = {};
/**
 * @license React
 * react.production.js
 *
 * Copyright (c) Meta Platforms, Inc. and affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
var nm;
function hg() {
    if (nm)
        return W;
    nm = 1;
    var s = Symbol.for("react.transitional.element")
      , d = Symbol.for("react.portal")
      , o = Symbol.for("react.fragment")
      , f = Symbol.for("react.strict_mode")
      , m = Symbol.for("react.profiler")
      , g = Symbol.for("react.consumer")
      , p = Symbol.for("react.context")
      , T = Symbol.for("react.forward_ref")
      , S = Symbol.for("react.suspense")
      , x = Symbol.for("react.memo")
      , N = Symbol.for("react.lazy")
      , _ = Symbol.for("react.activity")
      , H = Symbol.iterator;
    function U(v) {
        return v === null || typeof v != "object" ? null : (v = H && v[H] || v["@@iterator"],
        typeof v == "function" ? v : null)
    }
    var L = {
        isMounted: function() {
            return !1
        },
        enqueueForceUpdate: function() {},
        enqueueReplaceState: function() {},
        enqueueSetState: function() {}
    }
      , J = Object.assign
      , X = {};
    function Z(v, R, B) {
        this.props = v,
        this.context = R,
        this.refs = X,
        this.updater = B || L
    }
    Z.prototype.isReactComponent = {},
    Z.prototype.setState = function(v, R) {
        if (typeof v != "object" && typeof v != "function" && v != null)
            throw Error("takes an object of state variables to update or a function which returns an object of state variables.");
        this.updater.enqueueSetState(this, v, R, "setState")
    }
    ,
    Z.prototype.forceUpdate = function(v) {
        this.updater.enqueueForceUpdate(this, v, "forceUpdate")
    }
    ;
    function et() {}
    et.prototype = Z.prototype;
    function Y(v, R, B) {
        this.props = v,
        this.context = R,
        this.refs = X,
        this.updater = B || L
    }
    var dt = Y.prototype = new et;
    dt.constructor = Y,
    J(dt, Z.prototype),
    dt.isPureReactComponent = !0;
    var zt = Array.isArray;
    function qt() {}
    var P = {
        H: null,
        A: null,
        T: null,
        S: null
    }
      , Bt = Object.prototype.hasOwnProperty;
    function Tt(v, R, B) {
        var Q = B.ref;
        return {
            $$typeof: s,
            type: v,
            key: R,
            ref: Q !== void 0 ? Q : null,
            props: B
        }
    }
    function ie(v, R) {
        return Tt(v.type, R, v.props)
    }
    function ce(v) {
        return typeof v == "object" && v !== null && v.$$typeof === s
    }
    function Ft(v) {
        var R = {
            "=": "=0",
            ":": "=2"
        };
        return "$" + v.replace(/[=:]/g, function(B) {
            return R[B]
        })
    }
    var Rl = /\/+/g;
    function Ge(v, R) {
        return typeof v == "object" && v !== null && v.key != null ? Ft("" + v.key) : R.toString(36)
    }
    function Me(v) {
        switch (v.status) {
        case "fulfilled":
            return v.value;
        case "rejected":
            throw v.reason;
        default:
            switch (typeof v.status == "string" ? v.then(qt, qt) : (v.status = "pending",
            v.then(function(R) {
                v.status === "pending" && (v.status = "fulfilled",
                v.value = R)
            }, function(R) {
                v.status === "pending" && (v.status = "rejected",
                v.reason = R)
            })),
            v.status) {
            case "fulfilled":
                return v.value;
            case "rejected":
                throw v.reason
            }
        }
        throw v
    }
    function w(v, R, B, Q, F) {
        var lt = typeof v;
        (lt === "undefined" || lt === "boolean") && (v = null);
        var ot = !1;
        if (v === null)
            ot = !0;
        else
            switch (lt) {
            case "bigint":
            case "string":
            case "number":
                ot = !0;
                break;
            case "object":
                switch (v.$$typeof) {
                case s:
                case d:
                    ot = !0;
                    break;
                case N:
                    return ot = v._init,
                    w(ot(v._payload), R, B, Q, F)
                }
            }
        if (ot)
            return F = F(v),
            ot = Q === "" ? "." + Ge(v, 0) : Q,
            zt(F) ? (B = "",
            ot != null && (B = ot.replace(Rl, "$&/") + "/"),
            w(F, R, B, "", function(Qa) {
                return Qa
            })) : F != null && (ce(F) && (F = ie(F, B + (F.key == null || v && v.key === F.key ? "" : ("" + F.key).replace(Rl, "$&/") + "/") + ot)),
            R.push(F)),
            1;
        ot = 0;
        var $t = Q === "" ? "." : Q + ":";
        if (zt(v))
            for (var Ot = 0; Ot < v.length; Ot++)
                Q = v[Ot],
                lt = $t + Ge(Q, Ot),
                ot += w(Q, R, B, lt, F);
        else if (Ot = U(v),
        typeof Ot == "function")
            for (v = Ot.call(v),
            Ot = 0; !(Q = v.next()).done; )
                Q = Q.value,
                lt = $t + Ge(Q, Ot++),
                ot += w(Q, R, B, lt, F);
        else if (lt === "object") {
            if (typeof v.then == "function")
                return w(Me(v), R, B, Q, F);
            throw R = String(v),
            Error("Objects are not valid as a React child (found: " + (R === "[object Object]" ? "object with keys {" + Object.keys(v).join(", ") + "}" : R) + "). If you meant to render a collection of children, use an array instead.")
        }
        return ot
    }
    function q(v, R, B) {
        if (v == null)
            return v;
        var Q = []
          , F = 0;
        return w(v, Q, "", "", function(lt) {
            return R.call(B, lt, F++)
        }),
        Q
    }
    function $(v) {
        if (v._status === -1) {
            var R = v._result;
            R = R(),
            R.then(function(B) {
                (v._status === 0 || v._status === -1) && (v._status = 1,
                v._result = B)
            }, function(B) {
                (v._status === 0 || v._status === -1) && (v._status = 2,
                v._result = B)
            }),
            v._status === -1 && (v._status = 0,
            v._result = R)
        }
        if (v._status === 1)
            return v._result.default;
        throw v._result
    }
    var gt = typeof reportError == "function" ? reportError : function(v) {
        if (typeof window == "object" && typeof window.ErrorEvent == "function") {
            var R = new window.ErrorEvent("error",{
                bubbles: !0,
                cancelable: !0,
                message: typeof v == "object" && v !== null && typeof v.message == "string" ? String(v.message) : String(v),
                error: v
            });
            if (!window.dispatchEvent(R))
                return
        } else if (typeof process == "object" && typeof process.emit == "function") {
            process.emit("uncaughtException", v);
            return
        }
        console.error(v)
    }
      , pt = {
        map: q,
        forEach: function(v, R, B) {
            q(v, function() {
                R.apply(this, arguments)
            }, B)
        },
        count: function(v) {
            var R = 0;
            return q(v, function() {
                R++
            }),
            R
        },
        toArray: function(v) {
            return q(v, function(R) {
                return R
            }) || []
        },
        only: function(v) {
            if (!ce(v))
                throw Error("React.Children.only expected to receive a single React element child.");
            return v
        }
    };
    return W.Activity = _,
    W.Children = pt,
    W.Component = Z,
    W.Fragment = o,
    W.Profiler = m,
    W.PureComponent = Y,
    W.StrictMode = f,
    W.Suspense = S,
    W.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE = P,
    W.__COMPILER_RUNTIME = {
        __proto__: null,
        c: function(v) {
            return P.H.useMemoCache(v)
        }
    },
    W.cache = function(v) {
        return function() {
            return v.apply(null, arguments)
        }
    }
    ,
    W.cacheSignal = function() {
        return null
    }
    ,
    W.cloneElement = function(v, R, B) {
        if (v == null)
            throw Error("The argument must be a React element, but you passed " + v + ".");
        var Q = J({}, v.props)
          , F = v.key;
        if (R != null)
            for (lt in R.key !== void 0 && (F = "" + R.key),
            R)
                !Bt.call(R, lt) || lt === "key" || lt === "__self" || lt === "__source" || lt === "ref" && R.ref === void 0 || (Q[lt] = R[lt]);
        var lt = arguments.length - 2;
        if (lt === 1)
            Q.children = B;
        else if (1 < lt) {
            for (var ot = Array(lt), $t = 0; $t < lt; $t++)
                ot[$t] = arguments[$t + 2];
            Q.children = ot
        }
        return Tt(v.type, F, Q)
    }
    ,
    W.createContext = function(v) {
        return v = {
            $$typeof: p,
            _currentValue: v,
            _currentValue2: v,
            _threadCount: 0,
            Provider: null,
            Consumer: null
        },
        v.Provider = v,
        v.Consumer = {
            $$typeof: g,
            _context: v
        },
        v
    }
    ,
    W.createElement = function(v, R, B) {
        var Q, F = {}, lt = null;
        if (R != null)
            for (Q in R.key !== void 0 && (lt = "" + R.key),
            R)
                Bt.call(R, Q) && Q !== "key" && Q !== "__self" && Q !== "__source" && (F[Q] = R[Q]);
        var ot = arguments.length - 2;
        if (ot === 1)
            F.children = B;
        else if (1 < ot) {
            for (var $t = Array(ot), Ot = 0; Ot < ot; Ot++)
                $t[Ot] = arguments[Ot + 2];
            F.children = $t
        }
        if (v && v.defaultProps)
            for (Q in ot = v.defaultProps,
            ot)
                F[Q] === void 0 && (F[Q] = ot[Q]);
        return Tt(v, lt, F)
    }
    ,
    W.createRef = function() {
        return {
            current: null
        }
    }
    ,
    W.forwardRef = function(v) {
        return {
            $$typeof: T,
            render: v
        }
    }
    ,
    W.isValidElement = ce,
    W.lazy = function(v) {
        return {
            $$typeof: N,
            _payload: {
                _status: -1,
                _result: v
            },
            _init: $
        }
    }
    ,
    W.memo = function(v, R) {
        return {
            $$typeof: x,
            type: v,
            compare: R === void 0 ? null : R
        }
    }
    ,
    W.startTransition = function(v) {
        var R = P.T
          , B = {};
        P.T = B;
        try {
            var Q = v()
              , F = P.S;
            F !== null && F(B, Q),
            typeof Q == "object" && Q !== null && typeof Q.then == "function" && Q.then(qt, gt)
        } catch (lt) {
            gt(lt)
        } finally {
            R !== null && B.types !== null && (R.types = B.types),
            P.T = R
        }
    }
    ,
    W.unstable_useCacheRefresh = function() {
        return P.H.useCacheRefresh()
    }
    ,
    W.use = function(v) {
        return P.H.use(v)
    }
    ,
    W.useActionState = function(v, R, B) {
        return P.H.useActionState(v, R, B)
    }
    ,
    W.useCallback = function(v, R) {
        return P.H.useCallback(v, R)
    }
    ,
    W.useContext = function(v) {
        return P.H.useContext(v)
    }
    ,
    W.useDebugValue = function() {}
    ,
    W.useDeferredValue = function(v, R) {
        return P.H.useDeferredValue(v, R)
    }
    ,
    W.useEffect = function(v, R) {
        return P.H.useEffect(v, R)
    }
    ,
    W.useEffectEvent = function(v) {
        return P.H.useEffectEvent(v)
    }
    ,
    W.useId = function() {
        return P.H.useId()
    }
    ,
    W.useImperativeHandle = function(v, R, B) {
        return P.H.useImperativeHandle(v, R, B)
    }
    ,
    W.useInsertionEffect = function(v, R) {
        return P.H.useInsertionEffect(v, R)
    }
    ,
    W.useLayoutEffect = function(v, R) {
        return P.H.useLayoutEffect(v, R)
    }
    ,
    W.useMemo = function(v, R) {
        return P.H.useMemo(v, R)
    }
    ,
    W.useOptimistic = function(v, R) {
        return P.H.useOptimistic(v, R)
    }
    ,
    W.useReducer = function(v, R, B) {
        return P.H.useReducer(v, R, B)
    }
    ,
    W.useRef = function(v) {
        return P.H.useRef(v)
    }
    ,
    W.useState = function(v) {
        return P.H.useState(v)
    }
    ,
    W.useSyncExternalStore = function(v, R, B) {
        return P.H.useSyncExternalStore(v, R, B)
    }
    ,
    W.useTransition = function() {
        return P.H.useTransition()
    }
    ,
    W.version = "19.2.0",
    W
}
var um;
function Zs() {
    return um || (um = 1,
    Us.exports = hg()),
    Us.exports
}
var M = Zs();
const gg = Sm(M);
var Hs = {
    exports: {}
}
  , Bn = {}
  , qs = {
    exports: {}
}
  , Bs = {};
/**
 * @license React
 * scheduler.production.js
 *
 * Copyright (c) Meta Platforms, Inc. and affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
var im;
function xg() {
    return im || (im = 1,
    (function(s) {
        function d(w, q) {
            var $ = w.length;
            w.push(q);
            t: for (; 0 < $; ) {
                var gt = $ - 1 >>> 1
                  , pt = w[gt];
                if (0 < m(pt, q))
                    w[gt] = q,
                    w[$] = pt,
                    $ = gt;
                else
                    break t
            }
        }
        function o(w) {
            return w.length === 0 ? null : w[0]
        }
        function f(w) {
            if (w.length === 0)
                return null;
            var q = w[0]
              , $ = w.pop();
            if ($ !== q) {
                w[0] = $;
                t: for (var gt = 0, pt = w.length, v = pt >>> 1; gt < v; ) {
                    var R = 2 * (gt + 1) - 1
                      , B = w[R]
                      , Q = R + 1
                      , F = w[Q];
                    if (0 > m(B, $))
                        Q < pt && 0 > m(F, B) ? (w[gt] = F,
                        w[Q] = $,
                        gt = Q) : (w[gt] = B,
                        w[R] = $,
                        gt = R);
                    else if (Q < pt && 0 > m(F, $))
                        w[gt] = F,
                        w[Q] = $,
                        gt = Q;
                    else
                        break t
                }
            }
            return q
        }
        function m(w, q) {
            var $ = w.sortIndex - q.sortIndex;
            return $ !== 0 ? $ : w.id - q.id
        }
        if (s.unstable_now = void 0,
        typeof performance == "object" && typeof performance.now == "function") {
            var g = performance;
            s.unstable_now = function() {
                return g.now()
            }
        } else {
            var p = Date
              , T = p.now();
            s.unstable_now = function() {
                return p.now() - T
            }
        }
        var S = []
          , x = []
          , N = 1
          , _ = null
          , H = 3
          , U = !1
          , L = !1
          , J = !1
          , X = !1
          , Z = typeof setTimeout == "function" ? setTimeout : null
          , et = typeof clearTimeout == "function" ? clearTimeout : null
          , Y = typeof setImmediate < "u" ? setImmediate : null;
        function dt(w) {
            for (var q = o(x); q !== null; ) {
                if (q.callback === null)
                    f(x);
                else if (q.startTime <= w)
                    f(x),
                    q.sortIndex = q.expirationTime,
                    d(S, q);
                else
                    break;
                q = o(x)
            }
        }
        function zt(w) {
            if (J = !1,
            dt(w),
            !L)
                if (o(S) !== null)
                    L = !0,
                    qt || (qt = !0,
                    Ft());
                else {
                    var q = o(x);
                    q !== null && Me(zt, q.startTime - w)
                }
        }
        var qt = !1
          , P = -1
          , Bt = 5
          , Tt = -1;
        function ie() {
            return X ? !0 : !(s.unstable_now() - Tt < Bt)
        }
        function ce() {
            if (X = !1,
            qt) {
                var w = s.unstable_now();
                Tt = w;
                var q = !0;
                try {
                    t: {
                        L = !1,
                        J && (J = !1,
                        et(P),
                        P = -1),
                        U = !0;
                        var $ = H;
                        try {
                            e: {
                                for (dt(w),
                                _ = o(S); _ !== null && !(_.expirationTime > w && ie()); ) {
                                    var gt = _.callback;
                                    if (typeof gt == "function") {
                                        _.callback = null,
                                        H = _.priorityLevel;
                                        var pt = gt(_.expirationTime <= w);
                                        if (w = s.unstable_now(),
                                        typeof pt == "function") {
                                            _.callback = pt,
                                            dt(w),
                                            q = !0;
                                            break e
                                        }
                                        _ === o(S) && f(S),
                                        dt(w)
                                    } else
                                        f(S);
                                    _ = o(S)
                                }
                                if (_ !== null)
                                    q = !0;
                                else {
                                    var v = o(x);
                                    v !== null && Me(zt, v.startTime - w),
                                    q = !1
                                }
                            }
                            break t
                        } finally {
                            _ = null,
                            H = $,
                            U = !1
                        }
                        q = void 0
                    }
                } finally {
                    q ? Ft() : qt = !1
                }
            }
        }
        var Ft;
        if (typeof Y == "function")
            Ft = function() {
                Y(ce)
            }
            ;
        else if (typeof MessageChannel < "u") {
            var Rl = new MessageChannel
              , Ge = Rl.port2;
            Rl.port1.onmessage = ce,
            Ft = function() {
                Ge.postMessage(null)
            }
        } else
            Ft = function() {
                Z(ce, 0)
            }
            ;
        function Me(w, q) {
            P = Z(function() {
                w(s.unstable_now())
            }, q)
        }
        s.unstable_IdlePriority = 5,
        s.unstable_ImmediatePriority = 1,
        s.unstable_LowPriority = 4,
        s.unstable_NormalPriority = 3,
        s.unstable_Profiling = null,
        s.unstable_UserBlockingPriority = 2,
        s.unstable_cancelCallback = function(w) {
            w.callback = null
        }
        ,
        s.unstable_forceFrameRate = function(w) {
            0 > w || 125 < w ? console.error("forceFrameRate takes a positive int between 0 and 125, forcing frame rates higher than 125 fps is not supported") : Bt = 0 < w ? Math.floor(1e3 / w) : 5
        }
        ,
        s.unstable_getCurrentPriorityLevel = function() {
            return H
        }
        ,
        s.unstable_next = function(w) {
            switch (H) {
            case 1:
            case 2:
            case 3:
                var q = 3;
                break;
            default:
                q = H
            }
            var $ = H;
            H = q;
            try {
                return w()
            } finally {
                H = $
            }
        }
        ,
        s.unstable_requestPaint = function() {
            X = !0
        }
        ,
        s.unstable_runWithPriority = function(w, q) {
            switch (w) {
            case 1:
            case 2:
            case 3:
            case 4:
            case 5:
                break;
            default:
                w = 3
            }
            var $ = H;
            H = w;
            try {
                return q()
            } finally {
                H = $
            }
        }
        ,
        s.unstable_scheduleCallback = function(w, q, $) {
            var gt = s.unstable_now();
            switch (typeof $ == "object" && $ !== null ? ($ = $.delay,
            $ = typeof $ == "number" && 0 < $ ? gt + $ : gt) : $ = gt,
            w) {
            case 1:
                var pt = -1;
                break;
            case 2:
                pt = 250;
                break;
            case 5:
                pt = 1073741823;
                break;
            case 4:
                pt = 1e4;
                break;
            default:
                pt = 5e3
            }
            return pt = $ + pt,
            w = {
                id: N++,
                callback: q,
                priorityLevel: w,
                startTime: $,
                expirationTime: pt,
                sortIndex: -1
            },
            $ > gt ? (w.sortIndex = $,
            d(x, w),
            o(S) === null && w === o(x) && (J ? (et(P),
            P = -1) : J = !0,
            Me(zt, $ - gt))) : (w.sortIndex = pt,
            d(S, w),
            L || U || (L = !0,
            qt || (qt = !0,
            Ft()))),
            w
        }
        ,
        s.unstable_shouldYield = ie,
        s.unstable_wrapCallback = function(w) {
            var q = H;
            return function() {
                var $ = H;
                H = q;
                try {
                    return w.apply(this, arguments)
                } finally {
                    H = $
                }
            }
        }
    }
    )(Bs)),
    Bs
}
var cm;
function yg() {
    return cm || (cm = 1,
    qs.exports = xg()),
    qs.exports
}
var Ys = {
    exports: {}
}
  , kt = {};
/**
 * @license React
 * react-dom.production.js
 *
 * Copyright (c) Meta Platforms, Inc. and affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
var sm;
function vg() {
    if (sm)
        return kt;
    sm = 1;
    var s = Zs();
    function d(S) {
        var x = "https://react.dev/errors/" + S;
        if (1 < arguments.length) {
            x += "?args[]=" + encodeURIComponent(arguments[1]);
            for (var N = 2; N < arguments.length; N++)
                x += "&args[]=" + encodeURIComponent(arguments[N])
        }
        return "Minified React error #" + S + "; visit " + x + " for the full message or use the non-minified dev environment for full errors and additional helpful warnings."
    }
    function o() {}
    var f = {
        d: {
            f: o,
            r: function() {
                throw Error(d(522))
            },
            D: o,
            C: o,
            L: o,
            m: o,
            X: o,
            S: o,
            M: o
        },
        p: 0,
        findDOMNode: null
    }
      , m = Symbol.for("react.portal");
    function g(S, x, N) {
        var _ = 3 < arguments.length && arguments[3] !== void 0 ? arguments[3] : null;
        return {
            $$typeof: m,
            key: _ == null ? null : "" + _,
            children: S,
            containerInfo: x,
            implementation: N
        }
    }
    var p = s.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE;
    function T(S, x) {
        if (S === "font")
            return "";
        if (typeof x == "string")
            return x === "use-credentials" ? x : ""
    }
    return kt.__DOM_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE = f,
    kt.createPortal = function(S, x) {
        var N = 2 < arguments.length && arguments[2] !== void 0 ? arguments[2] : null;
        if (!x || x.nodeType !== 1 && x.nodeType !== 9 && x.nodeType !== 11)
            throw Error(d(299));
        return g(S, x, null, N)
    }
    ,
    kt.flushSync = function(S) {
        var x = p.T
          , N = f.p;
        try {
            if (p.T = null,
            f.p = 2,
            S)
                return S()
        } finally {
            p.T = x,
            f.p = N,
            f.d.f()
        }
    }
    ,
    kt.preconnect = function(S, x) {
        typeof S == "string" && (x ? (x = x.crossOrigin,
        x = typeof x == "string" ? x === "use-credentials" ? x : "" : void 0) : x = null,
        f.d.C(S, x))
    }
    ,
    kt.prefetchDNS = function(S) {
        typeof S == "string" && f.d.D(S)
    }
    ,
    kt.preinit = function(S, x) {
        if (typeof S == "string" && x && typeof x.as == "string") {
            var N = x.as
              , _ = T(N, x.crossOrigin)
              , H = typeof x.integrity == "string" ? x.integrity : void 0
              , U = typeof x.fetchPriority == "string" ? x.fetchPriority : void 0;
            N === "style" ? f.d.S(S, typeof x.precedence == "string" ? x.precedence : void 0, {
                crossOrigin: _,
                integrity: H,
                fetchPriority: U
            }) : N === "script" && f.d.X(S, {
                crossOrigin: _,
                integrity: H,
                fetchPriority: U,
                nonce: typeof x.nonce == "string" ? x.nonce : void 0
            })
        }
    }
    ,
    kt.preinitModule = function(S, x) {
        if (typeof S == "string")
            if (typeof x == "object" && x !== null) {
                if (x.as == null || x.as === "script") {
                    var N = T(x.as, x.crossOrigin);
                    f.d.M(S, {
                        crossOrigin: N,
                        integrity: typeof x.integrity == "string" ? x.integrity : void 0,
                        nonce: typeof x.nonce == "string" ? x.nonce : void 0
                    })
                }
            } else
                x == null && f.d.M(S)
    }
    ,
    kt.preload = function(S, x) {
        if (typeof S == "string" && typeof x == "object" && x !== null && typeof x.as == "string") {
            var N = x.as
              , _ = T(N, x.crossOrigin);
            f.d.L(S, N, {
                crossOrigin: _,
                integrity: typeof x.integrity == "string" ? x.integrity : void 0,
                nonce: typeof x.nonce == "string" ? x.nonce : void 0,
                type: typeof x.type == "string" ? x.type : void 0,
                fetchPriority: typeof x.fetchPriority == "string" ? x.fetchPriority : void 0,
                referrerPolicy: typeof x.referrerPolicy == "string" ? x.referrerPolicy : void 0,
                imageSrcSet: typeof x.imageSrcSet == "string" ? x.imageSrcSet : void 0,
                imageSizes: typeof x.imageSizes == "string" ? x.imageSizes : void 0,
                media: typeof x.media == "string" ? x.media : void 0
            })
        }
    }
    ,
    kt.preloadModule = function(S, x) {
        if (typeof S == "string")
            if (x) {
                var N = T(x.as, x.crossOrigin);
                f.d.m(S, {
                    as: typeof x.as == "string" && x.as !== "script" ? x.as : void 0,
                    crossOrigin: N,
                    integrity: typeof x.integrity == "string" ? x.integrity : void 0
                })
            } else
                f.d.m(S)
    }
    ,
    kt.requestFormReset = function(S) {
        f.d.r(S)
    }
    ,
    kt.unstable_batchedUpdates = function(S, x) {
        return S(x)
    }
    ,
    kt.useFormState = function(S, x, N) {
        return p.H.useFormState(S, x, N)
    }
    ,
    kt.useFormStatus = function() {
        return p.H.useHostTransitionStatus()
    }
    ,
    kt.version = "19.2.0",
    kt
}
var fm;
function pg() {
    if (fm)
        return Ys.exports;
    fm = 1;
    function s() {
        if (!(typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ > "u" || typeof __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE != "function"))
            try {
                __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE(s)
            } catch (d) {
                console.error(d)
            }
    }
    return s(),
    Ys.exports = vg(),
    Ys.exports
}
/**
 * @license React
 * react-dom-client.production.js
 *
 * Copyright (c) Meta Platforms, Inc. and affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
var rm;
function bg() {
    if (rm)
        return Bn;
    rm = 1;
    var s = yg()
      , d = Zs()
      , o = pg();
    function f(t) {
        var e = "https://react.dev/errors/" + t;
        if (1 < arguments.length) {
            e += "?args[]=" + encodeURIComponent(arguments[1]);
            for (var l = 2; l < arguments.length; l++)
                e += "&args[]=" + encodeURIComponent(arguments[l])
        }
        return "Minified React error #" + t + "; visit " + e + " for the full message or use the non-minified dev environment for full errors and additional helpful warnings."
    }
    function m(t) {
        return !(!t || t.nodeType !== 1 && t.nodeType !== 9 && t.nodeType !== 11)
    }
    function g(t) {
        var e = t
          , l = t;
        if (t.alternate)
            for (; e.return; )
                e = e.return;
        else {
            t = e;
            do
                e = t,
                (e.flags & 4098) !== 0 && (l = e.return),
                t = e.return;
            while (t)
        }
        return e.tag === 3 ? l : null
    }
    function p(t) {
        if (t.tag === 13) {
            var e = t.memoizedState;
            if (e === null && (t = t.alternate,
            t !== null && (e = t.memoizedState)),
            e !== null)
                return e.dehydrated
        }
        return null
    }
    function T(t) {
        if (t.tag === 31) {
            var e = t.memoizedState;
            if (e === null && (t = t.alternate,
            t !== null && (e = t.memoizedState)),
            e !== null)
                return e.dehydrated
        }
        return null
    }
    function S(t) {
        if (g(t) !== t)
            throw Error(f(188))
    }
    function x(t) {
        var e = t.alternate;
        if (!e) {
            if (e = g(t),
            e === null)
                throw Error(f(188));
            return e !== t ? null : t
        }
        for (var l = t, a = e; ; ) {
            var n = l.return;
            if (n === null)
                break;
            var u = n.alternate;
            if (u === null) {
                if (a = n.return,
                a !== null) {
                    l = a;
                    continue
                }
                break
            }
            if (n.child === u.child) {
                for (u = n.child; u; ) {
                    if (u === l)
                        return S(n),
                        t;
                    if (u === a)
                        return S(n),
                        e;
                    u = u.sibling
                }
                throw Error(f(188))
            }
            if (l.return !== a.return)
                l = n,
                a = u;
            else {
                for (var c = !1, r = n.child; r; ) {
                    if (r === l) {
                        c = !0,
                        l = n,
                        a = u;
                        break
                    }
                    if (r === a) {
                        c = !0,
                        a = n,
                        l = u;
                        break
                    }
                    r = r.sibling
                }
                if (!c) {
                    for (r = u.child; r; ) {
                        if (r === l) {
                            c = !0,
                            l = u,
                            a = n;
                            break
                        }
                        if (r === a) {
                            c = !0,
                            a = u,
                            l = n;
                            break
                        }
                        r = r.sibling
                    }
                    if (!c)
                        throw Error(f(189))
                }
            }
            if (l.alternate !== a)
                throw Error(f(190))
        }
        if (l.tag !== 3)
            throw Error(f(188));
        return l.stateNode.current === l ? t : e
    }
    function N(t) {
        var e = t.tag;
        if (e === 5 || e === 26 || e === 27 || e === 6)
            return t;
        for (t = t.child; t !== null; ) {
            if (e = N(t),
            e !== null)
                return e;
            t = t.sibling
        }
        return null
    }
    var _ = Object.assign
      , H = Symbol.for("react.element")
      , U = Symbol.for("react.transitional.element")
      , L = Symbol.for("react.portal")
      , J = Symbol.for("react.fragment")
      , X = Symbol.for("react.strict_mode")
      , Z = Symbol.for("react.profiler")
      , et = Symbol.for("react.consumer")
      , Y = Symbol.for("react.context")
      , dt = Symbol.for("react.forward_ref")
      , zt = Symbol.for("react.suspense")
      , qt = Symbol.for("react.suspense_list")
      , P = Symbol.for("react.memo")
      , Bt = Symbol.for("react.lazy")
      , Tt = Symbol.for("react.activity")
      , ie = Symbol.for("react.memo_cache_sentinel")
      , ce = Symbol.iterator;
    function Ft(t) {
        return t === null || typeof t != "object" ? null : (t = ce && t[ce] || t["@@iterator"],
        typeof t == "function" ? t : null)
    }
    var Rl = Symbol.for("react.client.reference");
    function Ge(t) {
        if (t == null)
            return null;
        if (typeof t == "function")
            return t.$$typeof === Rl ? null : t.displayName || t.name || null;
        if (typeof t == "string")
            return t;
        switch (t) {
        case J:
            return "Fragment";
        case Z:
            return "Profiler";
        case X:
            return "StrictMode";
        case zt:
            return "Suspense";
        case qt:
            return "SuspenseList";
        case Tt:
            return "Activity"
        }
        if (typeof t == "object")
            switch (t.$$typeof) {
            case L:
                return "Portal";
            case Y:
                return t.displayName || "Context";
            case et:
                return (t._context.displayName || "Context") + ".Consumer";
            case dt:
                var e = t.render;
                return t = t.displayName,
                t || (t = e.displayName || e.name || "",
                t = t !== "" ? "ForwardRef(" + t + ")" : "ForwardRef"),
                t;
            case P:
                return e = t.displayName || null,
                e !== null ? e : Ge(t.type) || "Memo";
            case Bt:
                e = t._payload,
                t = t._init;
                try {
                    return Ge(t(e))
                } catch {}
            }
        return null
    }
    var Me = Array.isArray
      , w = d.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE
      , q = o.__DOM_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE
      , $ = {
        pending: !1,
        data: null,
        method: null,
        action: null
    }
      , gt = []
      , pt = -1;
    function v(t) {
        return {
            current: t
        }
    }
    function R(t) {
        0 > pt || (t.current = gt[pt],
        gt[pt] = null,
        pt--)
    }
    function B(t, e) {
        pt++,
        gt[pt] = t.current,
        t.current = e
    }
    var Q = v(null)
      , F = v(null)
      , lt = v(null)
      , ot = v(null);
    function $t(t, e) {
        switch (B(lt, e),
        B(F, t),
        B(Q, null),
        e.nodeType) {
        case 9:
        case 11:
            t = (t = e.documentElement) && (t = t.namespaceURI) ? zd(t) : 0;
            break;
        default:
            if (t = e.tagName,
            e = e.namespaceURI)
                e = zd(e),
                t = Td(e, t);
            else
                switch (t) {
                case "svg":
                    t = 1;
                    break;
                case "math":
                    t = 2;
                    break;
                default:
                    t = 0
                }
        }
        R(Q),
        B(Q, t)
    }
    function Ot() {
        R(Q),
        R(F),
        R(lt)
    }
    function Qa(t) {
        t.memoizedState !== null && B(ot, t);
        var e = Q.current
          , l = Td(e, t.type);
        e !== l && (B(F, t),
        B(Q, l))
    }
    function Zn(t) {
        F.current === t && (R(Q),
        R(F)),
        ot.current === t && (R(ot),
        Cn._currentValue = $)
    }
    var xi, Ps;
    function Ul(t) {
        if (xi === void 0)
            try {
                throw Error()
            } catch (l) {
                var e = l.stack.trim().match(/\n( *(at )?)/);
                xi = e && e[1] || "",
                Ps = -1 < l.stack.indexOf(`
    at`) ? " (<anonymous>)" : -1 < l.stack.indexOf("@") ? "@unknown:0:0" : ""
            }
        return `
` + xi + t + Ps
    }
    var yi = !1;
    function vi(t, e) {
        if (!t || yi)
            return "";
        yi = !0;
        var l = Error.prepareStackTrace;
        Error.prepareStackTrace = void 0;
        try {
            var a = {
                DetermineComponentFrameRoot: function() {
                    try {
                        if (e) {
                            var C = function() {
                                throw Error()
                            };
                            if (Object.defineProperty(C.prototype, "props", {
                                set: function() {
                                    throw Error()
                                }
                            }),
                            typeof Reflect == "object" && Reflect.construct) {
                                try {
                                    Reflect.construct(C, [])
                                } catch (A) {
                                    var z = A
                                }
                                Reflect.construct(t, [], C)
                            } else {
                                try {
                                    C.call()
                                } catch (A) {
                                    z = A
                                }
                                t.call(C.prototype)
                            }
                        } else {
                            try {
                                throw Error()
                            } catch (A) {
                                z = A
                            }
                            (C = t()) && typeof C.catch == "function" && C.catch(function() {})
                        }
                    } catch (A) {
                        if (A && z && typeof A.stack == "string")
                            return [A.stack, z.stack]
                    }
                    return [null, null]
                }
            };
            a.DetermineComponentFrameRoot.displayName = "DetermineComponentFrameRoot";
            var n = Object.getOwnPropertyDescriptor(a.DetermineComponentFrameRoot, "name");
            n && n.configurable && Object.defineProperty(a.DetermineComponentFrameRoot, "name", {
                value: "DetermineComponentFrameRoot"
            });
            var u = a.DetermineComponentFrameRoot()
              , c = u[0]
              , r = u[1];
            if (c && r) {
                var h = c.split(`
`)
                  , E = r.split(`
`);
                for (n = a = 0; a < h.length && !h[a].includes("DetermineComponentFrameRoot"); )
                    a++;
                for (; n < E.length && !E[n].includes("DetermineComponentFrameRoot"); )
                    n++;
                if (a === h.length || n === E.length)
                    for (a = h.length - 1,
                    n = E.length - 1; 1 <= a && 0 <= n && h[a] !== E[n]; )
                        n--;
                for (; 1 <= a && 0 <= n; a--,
                n--)
                    if (h[a] !== E[n]) {
                        if (a !== 1 || n !== 1)
                            do
                                if (a--,
                                n--,
                                0 > n || h[a] !== E[n]) {
                                    var O = `
` + h[a].replace(" at new ", " at ");
                                    return t.displayName && O.includes("<anonymous>") && (O = O.replace("<anonymous>", t.displayName)),
                                    O
                                }
                            while (1 <= a && 0 <= n);
                        break
                    }
            }
        } finally {
            yi = !1,
            Error.prepareStackTrace = l
        }
        return (l = t ? t.displayName || t.name : "") ? Ul(l) : ""
    }
    function Qm(t, e) {
        switch (t.tag) {
        case 26:
        case 27:
        case 5:
            return Ul(t.type);
        case 16:
            return Ul("Lazy");
        case 13:
            return t.child !== e && e !== null ? Ul("Suspense Fallback") : Ul("Suspense");
        case 19:
            return Ul("SuspenseList");
        case 0:
        case 15:
            return vi(t.type, !1);
        case 11:
            return vi(t.type.render, !1);
        case 1:
            return vi(t.type, !0);
        case 31:
            return Ul("Activity");
        default:
            return ""
        }
    }
    function tf(t) {
        try {
            var e = ""
              , l = null;
            do
                e += Qm(t, l),
                l = t,
                t = t.return;
            while (t);
            return e
        } catch (a) {
            return `
Error generating stack: ` + a.message + `
` + a.stack
        }
    }
    var pi = Object.prototype.hasOwnProperty
      , bi = s.unstable_scheduleCallback
      , Si = s.unstable_cancelCallback
      , Zm = s.unstable_shouldYield
      , Vm = s.unstable_requestPaint
      , se = s.unstable_now
      , Km = s.unstable_getCurrentPriorityLevel
      , ef = s.unstable_ImmediatePriority
      , lf = s.unstable_UserBlockingPriority
      , Vn = s.unstable_NormalPriority
      , Jm = s.unstable_LowPriority
      , af = s.unstable_IdlePriority
      , km = s.log
      , $m = s.unstable_setDisableYieldValue
      , Za = null
      , fe = null;
    function fl(t) {
        if (typeof km == "function" && $m(t),
        fe && typeof fe.setStrictMode == "function")
            try {
                fe.setStrictMode(Za, t)
            } catch {}
    }
    var re = Math.clz32 ? Math.clz32 : Im
      , Wm = Math.log
      , Fm = Math.LN2;
    function Im(t) {
        return t >>>= 0,
        t === 0 ? 32 : 31 - (Wm(t) / Fm | 0) | 0
    }
    var Kn = 256
      , Jn = 262144
      , kn = 4194304;
    function Hl(t) {
        var e = t & 42;
        if (e !== 0)
            return e;
        switch (t & -t) {
        case 1:
            return 1;
        case 2:
            return 2;
        case 4:
            return 4;
        case 8:
            return 8;
        case 16:
            return 16;
        case 32:
            return 32;
        case 64:
            return 64;
        case 128:
            return 128;
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
            return t & 261888;
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
            return t & 3932160;
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
            return t & 62914560;
        case 67108864:
            return 67108864;
        case 134217728:
            return 134217728;
        case 268435456:
            return 268435456;
        case 536870912:
            return 536870912;
        case 1073741824:
            return 0;
        default:
            return t
        }
    }
    function $n(t, e, l) {
        var a = t.pendingLanes;
        if (a === 0)
            return 0;
        var n = 0
          , u = t.suspendedLanes
          , c = t.pingedLanes;
        t = t.warmLanes;
        var r = a & 134217727;
        return r !== 0 ? (a = r & ~u,
        a !== 0 ? n = Hl(a) : (c &= r,
        c !== 0 ? n = Hl(c) : l || (l = r & ~t,
        l !== 0 && (n = Hl(l))))) : (r = a & ~u,
        r !== 0 ? n = Hl(r) : c !== 0 ? n = Hl(c) : l || (l = a & ~t,
        l !== 0 && (n = Hl(l)))),
        n === 0 ? 0 : e !== 0 && e !== n && (e & u) === 0 && (u = n & -n,
        l = e & -e,
        u >= l || u === 32 && (l & 4194048) !== 0) ? e : n
    }
    function Va(t, e) {
        return (t.pendingLanes & ~(t.suspendedLanes & ~t.pingedLanes) & e) === 0
    }
    function Pm(t, e) {
        switch (t) {
        case 1:
        case 2:
        case 4:
        case 8:
        case 64:
            return e + 250;
        case 16:
        case 32:
        case 128:
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
            return e + 5e3;
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
            return -1;
        case 67108864:
        case 134217728:
        case 268435456:
        case 536870912:
        case 1073741824:
            return -1;
        default:
            return -1
        }
    }
    function nf() {
        var t = kn;
        return kn <<= 1,
        (kn & 62914560) === 0 && (kn = 4194304),
        t
    }
    function Ni(t) {
        for (var e = [], l = 0; 31 > l; l++)
            e.push(t);
        return e
    }
    function Ka(t, e) {
        t.pendingLanes |= e,
        e !== 268435456 && (t.suspendedLanes = 0,
        t.pingedLanes = 0,
        t.warmLanes = 0)
    }
    function th(t, e, l, a, n, u) {
        var c = t.pendingLanes;
        t.pendingLanes = l,
        t.suspendedLanes = 0,
        t.pingedLanes = 0,
        t.warmLanes = 0,
        t.expiredLanes &= l,
        t.entangledLanes &= l,
        t.errorRecoveryDisabledLanes &= l,
        t.shellSuspendCounter = 0;
        var r = t.entanglements
          , h = t.expirationTimes
          , E = t.hiddenUpdates;
        for (l = c & ~l; 0 < l; ) {
            var O = 31 - re(l)
              , C = 1 << O;
            r[O] = 0,
            h[O] = -1;
            var z = E[O];
            if (z !== null)
                for (E[O] = null,
                O = 0; O < z.length; O++) {
                    var A = z[O];
                    A !== null && (A.lane &= -536870913)
                }
            l &= ~C
        }
        a !== 0 && uf(t, a, 0),
        u !== 0 && n === 0 && t.tag !== 0 && (t.suspendedLanes |= u & ~(c & ~e))
    }
    function uf(t, e, l) {
        t.pendingLanes |= e,
        t.suspendedLanes &= ~e;
        var a = 31 - re(e);
        t.entangledLanes |= e,
        t.entanglements[a] = t.entanglements[a] | 1073741824 | l & 261930
    }
    function cf(t, e) {
        var l = t.entangledLanes |= e;
        for (t = t.entanglements; l; ) {
            var a = 31 - re(l)
              , n = 1 << a;
            n & e | t[a] & e && (t[a] |= e),
            l &= ~n
        }
    }
    function sf(t, e) {
        var l = e & -e;
        return l = (l & 42) !== 0 ? 1 : ji(l),
        (l & (t.suspendedLanes | e)) !== 0 ? 0 : l
    }
    function ji(t) {
        switch (t) {
        case 2:
            t = 1;
            break;
        case 8:
            t = 4;
            break;
        case 32:
            t = 16;
            break;
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
            t = 128;
            break;
        case 268435456:
            t = 134217728;
            break;
        default:
            t = 0
        }
        return t
    }
    function Ei(t) {
        return t &= -t,
        2 < t ? 8 < t ? (t & 134217727) !== 0 ? 32 : 268435456 : 8 : 2
    }
    function ff() {
        var t = q.p;
        return t !== 0 ? t : (t = window.event,
        t === void 0 ? 32 : $d(t.type))
    }
    function rf(t, e) {
        var l = q.p;
        try {
            return q.p = t,
            e()
        } finally {
            q.p = l
        }
    }
    var rl = Math.random().toString(36).slice(2)
      , Qt = "__reactFiber$" + rl
      , It = "__reactProps$" + rl
      , la = "__reactContainer$" + rl
      , zi = "__reactEvents$" + rl
      , eh = "__reactListeners$" + rl
      , lh = "__reactHandles$" + rl
      , of = "__reactResources$" + rl
      , Ja = "__reactMarker$" + rl;
    function Ti(t) {
        delete t[Qt],
        delete t[It],
        delete t[zi],
        delete t[eh],
        delete t[lh]
    }
    function aa(t) {
        var e = t[Qt];
        if (e)
            return e;
        for (var l = t.parentNode; l; ) {
            if (e = l[la] || l[Qt]) {
                if (l = e.alternate,
                e.child !== null || l !== null && l.child !== null)
                    for (t = Cd(t); t !== null; ) {
                        if (l = t[Qt])
                            return l;
                        t = Cd(t)
                    }
                return e
            }
            t = l,
            l = t.parentNode
        }
        return null
    }
    function na(t) {
        if (t = t[Qt] || t[la]) {
            var e = t.tag;
            if (e === 5 || e === 6 || e === 13 || e === 31 || e === 26 || e === 27 || e === 3)
                return t
        }
        return null
    }
    function ka(t) {
        var e = t.tag;
        if (e === 5 || e === 26 || e === 27 || e === 6)
            return t.stateNode;
        throw Error(f(33))
    }
    function ua(t) {
        var e = t[of];
        return e || (e = t[of] = {
            hoistableStyles: new Map,
            hoistableScripts: new Map
        }),
        e
    }
    function Gt(t) {
        t[Ja] = !0
    }
    var df = new Set
      , mf = {};
    function ql(t, e) {
        ia(t, e),
        ia(t + "Capture", e)
    }
    function ia(t, e) {
        for (mf[t] = e,
        t = 0; t < e.length; t++)
            df.add(e[t])
    }
    var ah = RegExp("^[:A-Z_a-z\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02FF\\u0370-\\u037D\\u037F-\\u1FFF\\u200C-\\u200D\\u2070-\\u218F\\u2C00-\\u2FEF\\u3001-\\uD7FF\\uF900-\\uFDCF\\uFDF0-\\uFFFD][:A-Z_a-z\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02FF\\u0370-\\u037D\\u037F-\\u1FFF\\u200C-\\u200D\\u2070-\\u218F\\u2C00-\\u2FEF\\u3001-\\uD7FF\\uF900-\\uFDCF\\uFDF0-\\uFFFD\\-.0-9\\u00B7\\u0300-\\u036F\\u203F-\\u2040]*$")
      , hf = {}
      , gf = {};
    function nh(t) {
        return pi.call(gf, t) ? !0 : pi.call(hf, t) ? !1 : ah.test(t) ? gf[t] = !0 : (hf[t] = !0,
        !1)
    }
    function Wn(t, e, l) {
        if (nh(e))
            if (l === null)
                t.removeAttribute(e);
            else {
                switch (typeof l) {
                case "undefined":
                case "function":
                case "symbol":
                    t.removeAttribute(e);
                    return;
                case "boolean":
                    var a = e.toLowerCase().slice(0, 5);
                    if (a !== "data-" && a !== "aria-") {
                        t.removeAttribute(e);
                        return
                    }
                }
                t.setAttribute(e, "" + l)
            }
    }
    function Fn(t, e, l) {
        if (l === null)
            t.removeAttribute(e);
        else {
            switch (typeof l) {
            case "undefined":
            case "function":
            case "symbol":
            case "boolean":
                t.removeAttribute(e);
                return
            }
            t.setAttribute(e, "" + l)
        }
    }
    function Xe(t, e, l, a) {
        if (a === null)
            t.removeAttribute(l);
        else {
            switch (typeof a) {
            case "undefined":
            case "function":
            case "symbol":
            case "boolean":
                t.removeAttribute(l);
                return
            }
            t.setAttributeNS(e, l, "" + a)
        }
    }
    function ve(t) {
        switch (typeof t) {
        case "bigint":
        case "boolean":
        case "number":
        case "string":
        case "undefined":
            return t;
        case "object":
            return t;
        default:
            return ""
        }
    }
    function xf(t) {
        var e = t.type;
        return (t = t.nodeName) && t.toLowerCase() === "input" && (e === "checkbox" || e === "radio")
    }
    function uh(t, e, l) {
        var a = Object.getOwnPropertyDescriptor(t.constructor.prototype, e);
        if (!t.hasOwnProperty(e) && typeof a < "u" && typeof a.get == "function" && typeof a.set == "function") {
            var n = a.get
              , u = a.set;
            return Object.defineProperty(t, e, {
                configurable: !0,
                get: function() {
                    return n.call(this)
                },
                set: function(c) {
                    l = "" + c,
                    u.call(this, c)
                }
            }),
            Object.defineProperty(t, e, {
                enumerable: a.enumerable
            }),
            {
                getValue: function() {
                    return l
                },
                setValue: function(c) {
                    l = "" + c
                },
                stopTracking: function() {
                    t._valueTracker = null,
                    delete t[e]
                }
            }
        }
    }
    function Ai(t) {
        if (!t._valueTracker) {
            var e = xf(t) ? "checked" : "value";
            t._valueTracker = uh(t, e, "" + t[e])
        }
    }
    function yf(t) {
        if (!t)
            return !1;
        var e = t._valueTracker;
        if (!e)
            return !0;
        var l = e.getValue()
          , a = "";
        return t && (a = xf(t) ? t.checked ? "true" : "false" : t.value),
        t = a,
        t !== l ? (e.setValue(t),
        !0) : !1
    }
    function In(t) {
        if (t = t || (typeof document < "u" ? document : void 0),
        typeof t > "u")
            return null;
        try {
            return t.activeElement || t.body
        } catch {
            return t.body
        }
    }
    var ih = /[\n"\\]/g;
    function pe(t) {
        return t.replace(ih, function(e) {
            return "\\" + e.charCodeAt(0).toString(16) + " "
        })
    }
    function _i(t, e, l, a, n, u, c, r) {
        t.name = "",
        c != null && typeof c != "function" && typeof c != "symbol" && typeof c != "boolean" ? t.type = c : t.removeAttribute("type"),
        e != null ? c === "number" ? (e === 0 && t.value === "" || t.value != e) && (t.value = "" + ve(e)) : t.value !== "" + ve(e) && (t.value = "" + ve(e)) : c !== "submit" && c !== "reset" || t.removeAttribute("value"),
        e != null ? Mi(t, c, ve(e)) : l != null ? Mi(t, c, ve(l)) : a != null && t.removeAttribute("value"),
        n == null && u != null && (t.defaultChecked = !!u),
        n != null && (t.checked = n && typeof n != "function" && typeof n != "symbol"),
        r != null && typeof r != "function" && typeof r != "symbol" && typeof r != "boolean" ? t.name = "" + ve(r) : t.removeAttribute("name")
    }
    function vf(t, e, l, a, n, u, c, r) {
        if (u != null && typeof u != "function" && typeof u != "symbol" && typeof u != "boolean" && (t.type = u),
        e != null || l != null) {
            if (!(u !== "submit" && u !== "reset" || e != null)) {
                Ai(t);
                return
            }
            l = l != null ? "" + ve(l) : "",
            e = e != null ? "" + ve(e) : l,
            r || e === t.value || (t.value = e),
            t.defaultValue = e
        }
        a = a ?? n,
        a = typeof a != "function" && typeof a != "symbol" && !!a,
        t.checked = r ? t.checked : !!a,
        t.defaultChecked = !!a,
        c != null && typeof c != "function" && typeof c != "symbol" && typeof c != "boolean" && (t.name = c),
        Ai(t)
    }
    function Mi(t, e, l) {
        e === "number" && In(t.ownerDocument) === t || t.defaultValue === "" + l || (t.defaultValue = "" + l)
    }
    function ca(t, e, l, a) {
        if (t = t.options,
        e) {
            e = {};
            for (var n = 0; n < l.length; n++)
                e["$" + l[n]] = !0;
            for (l = 0; l < t.length; l++)
                n = e.hasOwnProperty("$" + t[l].value),
                t[l].selected !== n && (t[l].selected = n),
                n && a && (t[l].defaultSelected = !0)
        } else {
            for (l = "" + ve(l),
            e = null,
            n = 0; n < t.length; n++) {
                if (t[n].value === l) {
                    t[n].selected = !0,
                    a && (t[n].defaultSelected = !0);
                    return
                }
                e !== null || t[n].disabled || (e = t[n])
            }
            e !== null && (e.selected = !0)
        }
    }
    function pf(t, e, l) {
        if (e != null && (e = "" + ve(e),
        e !== t.value && (t.value = e),
        l == null)) {
            t.defaultValue !== e && (t.defaultValue = e);
            return
        }
        t.defaultValue = l != null ? "" + ve(l) : ""
    }
    function bf(t, e, l, a) {
        if (e == null) {
            if (a != null) {
                if (l != null)
                    throw Error(f(92));
                if (Me(a)) {
                    if (1 < a.length)
                        throw Error(f(93));
                    a = a[0]
                }
                l = a
            }
            l == null && (l = ""),
            e = l
        }
        l = ve(e),
        t.defaultValue = l,
        a = t.textContent,
        a === l && a !== "" && a !== null && (t.value = a),
        Ai(t)
    }
    function sa(t, e) {
        if (e) {
            var l = t.firstChild;
            if (l && l === t.lastChild && l.nodeType === 3) {
                l.nodeValue = e;
                return
            }
        }
        t.textContent = e
    }
    var ch = new Set("animationIterationCount aspectRatio borderImageOutset borderImageSlice borderImageWidth boxFlex boxFlexGroup boxOrdinalGroup columnCount columns flex flexGrow flexPositive flexShrink flexNegative flexOrder gridArea gridRow gridRowEnd gridRowSpan gridRowStart gridColumn gridColumnEnd gridColumnSpan gridColumnStart fontWeight lineClamp lineHeight opacity order orphans scale tabSize widows zIndex zoom fillOpacity floodOpacity stopOpacity strokeDasharray strokeDashoffset strokeMiterlimit strokeOpacity strokeWidth MozAnimationIterationCount MozBoxFlex MozBoxFlexGroup MozLineClamp msAnimationIterationCount msFlex msZoom msFlexGrow msFlexNegative msFlexOrder msFlexPositive msFlexShrink msGridColumn msGridColumnSpan msGridRow msGridRowSpan WebkitAnimationIterationCount WebkitBoxFlex WebKitBoxFlexGroup WebkitBoxOrdinalGroup WebkitColumnCount WebkitColumns WebkitFlex WebkitFlexGrow WebkitFlexPositive WebkitFlexShrink WebkitLineClamp".split(" "));
    function Sf(t, e, l) {
        var a = e.indexOf("--") === 0;
        l == null || typeof l == "boolean" || l === "" ? a ? t.setProperty(e, "") : e === "float" ? t.cssFloat = "" : t[e] = "" : a ? t.setProperty(e, l) : typeof l != "number" || l === 0 || ch.has(e) ? e === "float" ? t.cssFloat = l : t[e] = ("" + l).trim() : t[e] = l + "px"
    }
    function Nf(t, e, l) {
        if (e != null && typeof e != "object")
            throw Error(f(62));
        if (t = t.style,
        l != null) {
            for (var a in l)
                !l.hasOwnProperty(a) || e != null && e.hasOwnProperty(a) || (a.indexOf("--") === 0 ? t.setProperty(a, "") : a === "float" ? t.cssFloat = "" : t[a] = "");
            for (var n in e)
                a = e[n],
                e.hasOwnProperty(n) && l[n] !== a && Sf(t, n, a)
        } else
            for (var u in e)
                e.hasOwnProperty(u) && Sf(t, u, e[u])
    }
    function Oi(t) {
        if (t.indexOf("-") === -1)
            return !1;
        switch (t) {
        case "annotation-xml":
        case "color-profile":
        case "font-face":
        case "font-face-src":
        case "font-face-uri":
        case "font-face-format":
        case "font-face-name":
        case "missing-glyph":
            return !1;
        default:
            return !0
        }
    }
    var sh = new Map([["acceptCharset", "accept-charset"], ["htmlFor", "for"], ["httpEquiv", "http-equiv"], ["crossOrigin", "crossorigin"], ["accentHeight", "accent-height"], ["alignmentBaseline", "alignment-baseline"], ["arabicForm", "arabic-form"], ["baselineShift", "baseline-shift"], ["capHeight", "cap-height"], ["clipPath", "clip-path"], ["clipRule", "clip-rule"], ["colorInterpolation", "color-interpolation"], ["colorInterpolationFilters", "color-interpolation-filters"], ["colorProfile", "color-profile"], ["colorRendering", "color-rendering"], ["dominantBaseline", "dominant-baseline"], ["enableBackground", "enable-background"], ["fillOpacity", "fill-opacity"], ["fillRule", "fill-rule"], ["floodColor", "flood-color"], ["floodOpacity", "flood-opacity"], ["fontFamily", "font-family"], ["fontSize", "font-size"], ["fontSizeAdjust", "font-size-adjust"], ["fontStretch", "font-stretch"], ["fontStyle", "font-style"], ["fontVariant", "font-variant"], ["fontWeight", "font-weight"], ["glyphName", "glyph-name"], ["glyphOrientationHorizontal", "glyph-orientation-horizontal"], ["glyphOrientationVertical", "glyph-orientation-vertical"], ["horizAdvX", "horiz-adv-x"], ["horizOriginX", "horiz-origin-x"], ["imageRendering", "image-rendering"], ["letterSpacing", "letter-spacing"], ["lightingColor", "lighting-color"], ["markerEnd", "marker-end"], ["markerMid", "marker-mid"], ["markerStart", "marker-start"], ["overlinePosition", "overline-position"], ["overlineThickness", "overline-thickness"], ["paintOrder", "paint-order"], ["panose-1", "panose-1"], ["pointerEvents", "pointer-events"], ["renderingIntent", "rendering-intent"], ["shapeRendering", "shape-rendering"], ["stopColor", "stop-color"], ["stopOpacity", "stop-opacity"], ["strikethroughPosition", "strikethrough-position"], ["strikethroughThickness", "strikethrough-thickness"], ["strokeDasharray", "stroke-dasharray"], ["strokeDashoffset", "stroke-dashoffset"], ["strokeLinecap", "stroke-linecap"], ["strokeLinejoin", "stroke-linejoin"], ["strokeMiterlimit", "stroke-miterlimit"], ["strokeOpacity", "stroke-opacity"], ["strokeWidth", "stroke-width"], ["textAnchor", "text-anchor"], ["textDecoration", "text-decoration"], ["textRendering", "text-rendering"], ["transformOrigin", "transform-origin"], ["underlinePosition", "underline-position"], ["underlineThickness", "underline-thickness"], ["unicodeBidi", "unicode-bidi"], ["unicodeRange", "unicode-range"], ["unitsPerEm", "units-per-em"], ["vAlphabetic", "v-alphabetic"], ["vHanging", "v-hanging"], ["vIdeographic", "v-ideographic"], ["vMathematical", "v-mathematical"], ["vectorEffect", "vector-effect"], ["vertAdvY", "vert-adv-y"], ["vertOriginX", "vert-origin-x"], ["vertOriginY", "vert-origin-y"], ["wordSpacing", "word-spacing"], ["writingMode", "writing-mode"], ["xmlnsXlink", "xmlns:xlink"], ["xHeight", "x-height"]])
      , fh = /^[\u0000-\u001F ]*j[\r\n\t]*a[\r\n\t]*v[\r\n\t]*a[\r\n\t]*s[\r\n\t]*c[\r\n\t]*r[\r\n\t]*i[\r\n\t]*p[\r\n\t]*t[\r\n\t]*:/i;
    function Pn(t) {
        return fh.test("" + t) ? "javascript:throw new Error('React has blocked a javascript: URL as a security precaution.')" : t
    }
    function Qe() {}
    var wi = null;
    function Di(t) {
        return t = t.target || t.srcElement || window,
        t.correspondingUseElement && (t = t.correspondingUseElement),
        t.nodeType === 3 ? t.parentNode : t
    }
    var fa = null
      , ra = null;
    function jf(t) {
        var e = na(t);
        if (e && (t = e.stateNode)) {
            var l = t[It] || null;
            t: switch (t = e.stateNode,
            e.type) {
            case "input":
                if (_i(t, l.value, l.defaultValue, l.defaultValue, l.checked, l.defaultChecked, l.type, l.name),
                e = l.name,
                l.type === "radio" && e != null) {
                    for (l = t; l.parentNode; )
                        l = l.parentNode;
                    for (l = l.querySelectorAll('input[name="' + pe("" + e) + '"][type="radio"]'),
                    e = 0; e < l.length; e++) {
                        var a = l[e];
                        if (a !== t && a.form === t.form) {
                            var n = a[It] || null;
                            if (!n)
                                throw Error(f(90));
                            _i(a, n.value, n.defaultValue, n.defaultValue, n.checked, n.defaultChecked, n.type, n.name)
                        }
                    }
                    for (e = 0; e < l.length; e++)
                        a = l[e],
                        a.form === t.form && yf(a)
                }
                break t;
            case "textarea":
                pf(t, l.value, l.defaultValue);
                break t;
            case "select":
                e = l.value,
                e != null && ca(t, !!l.multiple, e, !1)
            }
        }
    }
    var Ci = !1;
    function Ef(t, e, l) {
        if (Ci)
            return t(e, l);
        Ci = !0;
        try {
            var a = t(e);
            return a
        } finally {
            if (Ci = !1,
            (fa !== null || ra !== null) && (Lu(),
            fa && (e = fa,
            t = ra,
            ra = fa = null,
            jf(e),
            t)))
                for (e = 0; e < t.length; e++)
                    jf(t[e])
        }
    }
    function $a(t, e) {
        var l = t.stateNode;
        if (l === null)
            return null;
        var a = l[It] || null;
        if (a === null)
            return null;
        l = a[e];
        t: switch (e) {
        case "onClick":
        case "onClickCapture":
        case "onDoubleClick":
        case "onDoubleClickCapture":
        case "onMouseDown":
        case "onMouseDownCapture":
        case "onMouseMove":
        case "onMouseMoveCapture":
        case "onMouseUp":
        case "onMouseUpCapture":
        case "onMouseEnter":
            (a = !a.disabled) || (t = t.type,
            a = !(t === "button" || t === "input" || t === "select" || t === "textarea")),
            t = !a;
            break t;
        default:
            t = !1
        }
        if (t)
            return null;
        if (l && typeof l != "function")
            throw Error(f(231, e, typeof l));
        return l
    }
    var Ze = !(typeof window > "u" || typeof window.document > "u" || typeof window.document.createElement > "u")
      , Ri = !1;
    if (Ze)
        try {
            var Wa = {};
            Object.defineProperty(Wa, "passive", {
                get: function() {
                    Ri = !0
                }
            }),
            window.addEventListener("test", Wa, Wa),
            window.removeEventListener("test", Wa, Wa)
        } catch {
            Ri = !1
        }
    var ol = null
      , Ui = null
      , tu = null;
    function zf() {
        if (tu)
            return tu;
        var t, e = Ui, l = e.length, a, n = "value"in ol ? ol.value : ol.textContent, u = n.length;
        for (t = 0; t < l && e[t] === n[t]; t++)
            ;
        var c = l - t;
        for (a = 1; a <= c && e[l - a] === n[u - a]; a++)
            ;
        return tu = n.slice(t, 1 < a ? 1 - a : void 0)
    }
    function eu(t) {
        var e = t.keyCode;
        return "charCode"in t ? (t = t.charCode,
        t === 0 && e === 13 && (t = 13)) : t = e,
        t === 10 && (t = 13),
        32 <= t || t === 13 ? t : 0
    }
    function lu() {
        return !0
    }
    function Tf() {
        return !1
    }
    function Pt(t) {
        function e(l, a, n, u, c) {
            this._reactName = l,
            this._targetInst = n,
            this.type = a,
            this.nativeEvent = u,
            this.target = c,
            this.currentTarget = null;
            for (var r in t)
                t.hasOwnProperty(r) && (l = t[r],
                this[r] = l ? l(u) : u[r]);
            return this.isDefaultPrevented = (u.defaultPrevented != null ? u.defaultPrevented : u.returnValue === !1) ? lu : Tf,
            this.isPropagationStopped = Tf,
            this
        }
        return _(e.prototype, {
            preventDefault: function() {
                this.defaultPrevented = !0;
                var l = this.nativeEvent;
                l && (l.preventDefault ? l.preventDefault() : typeof l.returnValue != "unknown" && (l.returnValue = !1),
                this.isDefaultPrevented = lu)
            },
            stopPropagation: function() {
                var l = this.nativeEvent;
                l && (l.stopPropagation ? l.stopPropagation() : typeof l.cancelBubble != "unknown" && (l.cancelBubble = !0),
                this.isPropagationStopped = lu)
            },
            persist: function() {},
            isPersistent: lu
        }),
        e
    }
    var Bl = {
        eventPhase: 0,
        bubbles: 0,
        cancelable: 0,
        timeStamp: function(t) {
            return t.timeStamp || Date.now()
        },
        defaultPrevented: 0,
        isTrusted: 0
    }, au = Pt(Bl), Fa = _({}, Bl, {
        view: 0,
        detail: 0
    }), rh = Pt(Fa), Hi, qi, Ia, nu = _({}, Fa, {
        screenX: 0,
        screenY: 0,
        clientX: 0,
        clientY: 0,
        pageX: 0,
        pageY: 0,
        ctrlKey: 0,
        shiftKey: 0,
        altKey: 0,
        metaKey: 0,
        getModifierState: Yi,
        button: 0,
        buttons: 0,
        relatedTarget: function(t) {
            return t.relatedTarget === void 0 ? t.fromElement === t.srcElement ? t.toElement : t.fromElement : t.relatedTarget
        },
        movementX: function(t) {
            return "movementX"in t ? t.movementX : (t !== Ia && (Ia && t.type === "mousemove" ? (Hi = t.screenX - Ia.screenX,
            qi = t.screenY - Ia.screenY) : qi = Hi = 0,
            Ia = t),
            Hi)
        },
        movementY: function(t) {
            return "movementY"in t ? t.movementY : qi
        }
    }), Af = Pt(nu), oh = _({}, nu, {
        dataTransfer: 0
    }), dh = Pt(oh), mh = _({}, Fa, {
        relatedTarget: 0
    }), Bi = Pt(mh), hh = _({}, Bl, {
        animationName: 0,
        elapsedTime: 0,
        pseudoElement: 0
    }), gh = Pt(hh), xh = _({}, Bl, {
        clipboardData: function(t) {
            return "clipboardData"in t ? t.clipboardData : window.clipboardData
        }
    }), yh = Pt(xh), vh = _({}, Bl, {
        data: 0
    }), _f = Pt(vh), ph = {
        Esc: "Escape",
        Spacebar: " ",
        Left: "ArrowLeft",
        Up: "ArrowUp",
        Right: "ArrowRight",
        Down: "ArrowDown",
        Del: "Delete",
        Win: "OS",
        Menu: "ContextMenu",
        Apps: "ContextMenu",
        Scroll: "ScrollLock",
        MozPrintableKey: "Unidentified"
    }, bh = {
        8: "Backspace",
        9: "Tab",
        12: "Clear",
        13: "Enter",
        16: "Shift",
        17: "Control",
        18: "Alt",
        19: "Pause",
        20: "CapsLock",
        27: "Escape",
        32: " ",
        33: "PageUp",
        34: "PageDown",
        35: "End",
        36: "Home",
        37: "ArrowLeft",
        38: "ArrowUp",
        39: "ArrowRight",
        40: "ArrowDown",
        45: "Insert",
        46: "Delete",
        112: "F1",
        113: "F2",
        114: "F3",
        115: "F4",
        116: "F5",
        117: "F6",
        118: "F7",
        119: "F8",
        120: "F9",
        121: "F10",
        122: "F11",
        123: "F12",
        144: "NumLock",
        145: "ScrollLock",
        224: "Meta"
    }, Sh = {
        Alt: "altKey",
        Control: "ctrlKey",
        Meta: "metaKey",
        Shift: "shiftKey"
    };
    function Nh(t) {
        var e = this.nativeEvent;
        return e.getModifierState ? e.getModifierState(t) : (t = Sh[t]) ? !!e[t] : !1
    }
    function Yi() {
        return Nh
    }
    var jh = _({}, Fa, {
        key: function(t) {
            if (t.key) {
                var e = ph[t.key] || t.key;
                if (e !== "Unidentified")
                    return e
            }
            return t.type === "keypress" ? (t = eu(t),
            t === 13 ? "Enter" : String.fromCharCode(t)) : t.type === "keydown" || t.type === "keyup" ? bh[t.keyCode] || "Unidentified" : ""
        },
        code: 0,
        location: 0,
        ctrlKey: 0,
        shiftKey: 0,
        altKey: 0,
        metaKey: 0,
        repeat: 0,
        locale: 0,
        getModifierState: Yi,
        charCode: function(t) {
            return t.type === "keypress" ? eu(t) : 0
        },
        keyCode: function(t) {
            return t.type === "keydown" || t.type === "keyup" ? t.keyCode : 0
        },
        which: function(t) {
            return t.type === "keypress" ? eu(t) : t.type === "keydown" || t.type === "keyup" ? t.keyCode : 0
        }
    })
      , Eh = Pt(jh)
      , zh = _({}, nu, {
        pointerId: 0,
        width: 0,
        height: 0,
        pressure: 0,
        tangentialPressure: 0,
        tiltX: 0,
        tiltY: 0,
        twist: 0,
        pointerType: 0,
        isPrimary: 0
    })
      , Mf = Pt(zh)
      , Th = _({}, Fa, {
        touches: 0,
        targetTouches: 0,
        changedTouches: 0,
        altKey: 0,
        metaKey: 0,
        ctrlKey: 0,
        shiftKey: 0,
        getModifierState: Yi
    })
      , Ah = Pt(Th)
      , _h = _({}, Bl, {
        propertyName: 0,
        elapsedTime: 0,
        pseudoElement: 0
    })
      , Mh = Pt(_h)
      , Oh = _({}, nu, {
        deltaX: function(t) {
            return "deltaX"in t ? t.deltaX : "wheelDeltaX"in t ? -t.wheelDeltaX : 0
        },
        deltaY: function(t) {
            return "deltaY"in t ? t.deltaY : "wheelDeltaY"in t ? -t.wheelDeltaY : "wheelDelta"in t ? -t.wheelDelta : 0
        },
        deltaZ: 0,
        deltaMode: 0
    })
      , wh = Pt(Oh)
      , Dh = _({}, Bl, {
        newState: 0,
        oldState: 0
    })
      , Ch = Pt(Dh)
      , Rh = [9, 13, 27, 32]
      , Li = Ze && "CompositionEvent"in window
      , Pa = null;
    Ze && "documentMode"in document && (Pa = document.documentMode);
    var Uh = Ze && "TextEvent"in window && !Pa
      , Of = Ze && (!Li || Pa && 8 < Pa && 11 >= Pa)
      , wf = " "
      , Df = !1;
    function Cf(t, e) {
        switch (t) {
        case "keyup":
            return Rh.indexOf(e.keyCode) !== -1;
        case "keydown":
            return e.keyCode !== 229;
        case "keypress":
        case "mousedown":
        case "focusout":
            return !0;
        default:
            return !1
        }
    }
    function Rf(t) {
        return t = t.detail,
        typeof t == "object" && "data"in t ? t.data : null
    }
    var oa = !1;
    function Hh(t, e) {
        switch (t) {
        case "compositionend":
            return Rf(e);
        case "keypress":
            return e.which !== 32 ? null : (Df = !0,
            wf);
        case "textInput":
            return t = e.data,
            t === wf && Df ? null : t;
        default:
            return null
        }
    }
    function qh(t, e) {
        if (oa)
            return t === "compositionend" || !Li && Cf(t, e) ? (t = zf(),
            tu = Ui = ol = null,
            oa = !1,
            t) : null;
        switch (t) {
        case "paste":
            return null;
        case "keypress":
            if (!(e.ctrlKey || e.altKey || e.metaKey) || e.ctrlKey && e.altKey) {
                if (e.char && 1 < e.char.length)
                    return e.char;
                if (e.which)
                    return String.fromCharCode(e.which)
            }
            return null;
        case "compositionend":
            return Of && e.locale !== "ko" ? null : e.data;
        default:
            return null
        }
    }
    var Bh = {
        color: !0,
        date: !0,
        datetime: !0,
        "datetime-local": !0,
        email: !0,
        month: !0,
        number: !0,
        password: !0,
        range: !0,
        search: !0,
        tel: !0,
        text: !0,
        time: !0,
        url: !0,
        week: !0
    };
    function Uf(t) {
        var e = t && t.nodeName && t.nodeName.toLowerCase();
        return e === "input" ? !!Bh[t.type] : e === "textarea"
    }
    function Hf(t, e, l, a) {
        fa ? ra ? ra.push(a) : ra = [a] : fa = a,
        e = Ju(e, "onChange"),
        0 < e.length && (l = new au("onChange","change",null,l,a),
        t.push({
            event: l,
            listeners: e
        }))
    }
    var tn = null
      , en = null;
    function Yh(t) {
        pd(t, 0)
    }
    function uu(t) {
        var e = ka(t);
        if (yf(e))
            return t
    }
    function qf(t, e) {
        if (t === "change")
            return e
    }
    var Bf = !1;
    if (Ze) {
        var Gi;
        if (Ze) {
            var Xi = "oninput"in document;
            if (!Xi) {
                var Yf = document.createElement("div");
                Yf.setAttribute("oninput", "return;"),
                Xi = typeof Yf.oninput == "function"
            }
            Gi = Xi
        } else
            Gi = !1;
        Bf = Gi && (!document.documentMode || 9 < document.documentMode)
    }
    function Lf() {
        tn && (tn.detachEvent("onpropertychange", Gf),
        en = tn = null)
    }
    function Gf(t) {
        if (t.propertyName === "value" && uu(en)) {
            var e = [];
            Hf(e, en, t, Di(t)),
            Ef(Yh, e)
        }
    }
    function Lh(t, e, l) {
        t === "focusin" ? (Lf(),
        tn = e,
        en = l,
        tn.attachEvent("onpropertychange", Gf)) : t === "focusout" && Lf()
    }
    function Gh(t) {
        if (t === "selectionchange" || t === "keyup" || t === "keydown")
            return uu(en)
    }
    function Xh(t, e) {
        if (t === "click")
            return uu(e)
    }
    function Qh(t, e) {
        if (t === "input" || t === "change")
            return uu(e)
    }
    function Zh(t, e) {
        return t === e && (t !== 0 || 1 / t === 1 / e) || t !== t && e !== e
    }
    var oe = typeof Object.is == "function" ? Object.is : Zh;
    function ln(t, e) {
        if (oe(t, e))
            return !0;
        if (typeof t != "object" || t === null || typeof e != "object" || e === null)
            return !1;
        var l = Object.keys(t)
          , a = Object.keys(e);
        if (l.length !== a.length)
            return !1;
        for (a = 0; a < l.length; a++) {
            var n = l[a];
            if (!pi.call(e, n) || !oe(t[n], e[n]))
                return !1
        }
        return !0
    }
    function Xf(t) {
        for (; t && t.firstChild; )
            t = t.firstChild;
        return t
    }
    function Qf(t, e) {
        var l = Xf(t);
        t = 0;
        for (var a; l; ) {
            if (l.nodeType === 3) {
                if (a = t + l.textContent.length,
                t <= e && a >= e)
                    return {
                        node: l,
                        offset: e - t
                    };
                t = a
            }
            t: {
                for (; l; ) {
                    if (l.nextSibling) {
                        l = l.nextSibling;
                        break t
                    }
                    l = l.parentNode
                }
                l = void 0
            }
            l = Xf(l)
        }
    }
    function Zf(t, e) {
        return t && e ? t === e ? !0 : t && t.nodeType === 3 ? !1 : e && e.nodeType === 3 ? Zf(t, e.parentNode) : "contains"in t ? t.contains(e) : t.compareDocumentPosition ? !!(t.compareDocumentPosition(e) & 16) : !1 : !1
    }
    function Vf(t) {
        t = t != null && t.ownerDocument != null && t.ownerDocument.defaultView != null ? t.ownerDocument.defaultView : window;
        for (var e = In(t.document); e instanceof t.HTMLIFrameElement; ) {
            try {
                var l = typeof e.contentWindow.location.href == "string"
            } catch {
                l = !1
            }
            if (l)
                t = e.contentWindow;
            else
                break;
            e = In(t.document)
        }
        return e
    }
    function Qi(t) {
        var e = t && t.nodeName && t.nodeName.toLowerCase();
        return e && (e === "input" && (t.type === "text" || t.type === "search" || t.type === "tel" || t.type === "url" || t.type === "password") || e === "textarea" || t.contentEditable === "true")
    }
    var Vh = Ze && "documentMode"in document && 11 >= document.documentMode
      , da = null
      , Zi = null
      , an = null
      , Vi = !1;
    function Kf(t, e, l) {
        var a = l.window === l ? l.document : l.nodeType === 9 ? l : l.ownerDocument;
        Vi || da == null || da !== In(a) || (a = da,
        "selectionStart"in a && Qi(a) ? a = {
            start: a.selectionStart,
            end: a.selectionEnd
        } : (a = (a.ownerDocument && a.ownerDocument.defaultView || window).getSelection(),
        a = {
            anchorNode: a.anchorNode,
            anchorOffset: a.anchorOffset,
            focusNode: a.focusNode,
            focusOffset: a.focusOffset
        }),
        an && ln(an, a) || (an = a,
        a = Ju(Zi, "onSelect"),
        0 < a.length && (e = new au("onSelect","select",null,e,l),
        t.push({
            event: e,
            listeners: a
        }),
        e.target = da)))
    }
    function Yl(t, e) {
        var l = {};
        return l[t.toLowerCase()] = e.toLowerCase(),
        l["Webkit" + t] = "webkit" + e,
        l["Moz" + t] = "moz" + e,
        l
    }
    var ma = {
        animationend: Yl("Animation", "AnimationEnd"),
        animationiteration: Yl("Animation", "AnimationIteration"),
        animationstart: Yl("Animation", "AnimationStart"),
        transitionrun: Yl("Transition", "TransitionRun"),
        transitionstart: Yl("Transition", "TransitionStart"),
        transitioncancel: Yl("Transition", "TransitionCancel"),
        transitionend: Yl("Transition", "TransitionEnd")
    }
      , Ki = {}
      , Jf = {};
    Ze && (Jf = document.createElement("div").style,
    "AnimationEvent"in window || (delete ma.animationend.animation,
    delete ma.animationiteration.animation,
    delete ma.animationstart.animation),
    "TransitionEvent"in window || delete ma.transitionend.transition);
    function Ll(t) {
        if (Ki[t])
            return Ki[t];
        if (!ma[t])
            return t;
        var e = ma[t], l;
        for (l in e)
            if (e.hasOwnProperty(l) && l in Jf)
                return Ki[t] = e[l];
        return t
    }
    var kf = Ll("animationend")
      , $f = Ll("animationiteration")
      , Wf = Ll("animationstart")
      , Kh = Ll("transitionrun")
      , Jh = Ll("transitionstart")
      , kh = Ll("transitioncancel")
      , Ff = Ll("transitionend")
      , If = new Map
      , Ji = "abort auxClick beforeToggle cancel canPlay canPlayThrough click close contextMenu copy cut drag dragEnd dragEnter dragExit dragLeave dragOver dragStart drop durationChange emptied encrypted ended error gotPointerCapture input invalid keyDown keyPress keyUp load loadedData loadedMetadata loadStart lostPointerCapture mouseDown mouseMove mouseOut mouseOver mouseUp paste pause play playing pointerCancel pointerDown pointerMove pointerOut pointerOver pointerUp progress rateChange reset resize seeked seeking stalled submit suspend timeUpdate touchCancel touchEnd touchStart volumeChange scroll toggle touchMove waiting wheel".split(" ");
    Ji.push("scrollEnd");
    function Oe(t, e) {
        If.set(t, e),
        ql(e, [t])
    }
    var iu = typeof reportError == "function" ? reportError : function(t) {
        if (typeof window == "object" && typeof window.ErrorEvent == "function") {
            var e = new window.ErrorEvent("error",{
                bubbles: !0,
                cancelable: !0,
                message: typeof t == "object" && t !== null && typeof t.message == "string" ? String(t.message) : String(t),
                error: t
            });
            if (!window.dispatchEvent(e))
                return
        } else if (typeof process == "object" && typeof process.emit == "function") {
            process.emit("uncaughtException", t);
            return
        }
        console.error(t)
    }
      , be = []
      , ha = 0
      , ki = 0;
    function cu() {
        for (var t = ha, e = ki = ha = 0; e < t; ) {
            var l = be[e];
            be[e++] = null;
            var a = be[e];
            be[e++] = null;
            var n = be[e];
            be[e++] = null;
            var u = be[e];
            if (be[e++] = null,
            a !== null && n !== null) {
                var c = a.pending;
                c === null ? n.next = n : (n.next = c.next,
                c.next = n),
                a.pending = n
            }
            u !== 0 && Pf(l, n, u)
        }
    }
    function su(t, e, l, a) {
        be[ha++] = t,
        be[ha++] = e,
        be[ha++] = l,
        be[ha++] = a,
        ki |= a,
        t.lanes |= a,
        t = t.alternate,
        t !== null && (t.lanes |= a)
    }
    function $i(t, e, l, a) {
        return su(t, e, l, a),
        fu(t)
    }
    function Gl(t, e) {
        return su(t, null, null, e),
        fu(t)
    }
    function Pf(t, e, l) {
        t.lanes |= l;
        var a = t.alternate;
        a !== null && (a.lanes |= l);
        for (var n = !1, u = t.return; u !== null; )
            u.childLanes |= l,
            a = u.alternate,
            a !== null && (a.childLanes |= l),
            u.tag === 22 && (t = u.stateNode,
            t === null || t._visibility & 1 || (n = !0)),
            t = u,
            u = u.return;
        return t.tag === 3 ? (u = t.stateNode,
        n && e !== null && (n = 31 - re(l),
        t = u.hiddenUpdates,
        a = t[n],
        a === null ? t[n] = [e] : a.push(e),
        e.lane = l | 536870912),
        u) : null
    }
    function fu(t) {
        if (50 < Tn)
            throw Tn = 0,
            ns = null,
            Error(f(185));
        for (var e = t.return; e !== null; )
            t = e,
            e = t.return;
        return t.tag === 3 ? t.stateNode : null
    }
    var ga = {};
    function $h(t, e, l, a) {
        this.tag = t,
        this.key = l,
        this.sibling = this.child = this.return = this.stateNode = this.type = this.elementType = null,
        this.index = 0,
        this.refCleanup = this.ref = null,
        this.pendingProps = e,
        this.dependencies = this.memoizedState = this.updateQueue = this.memoizedProps = null,
        this.mode = a,
        this.subtreeFlags = this.flags = 0,
        this.deletions = null,
        this.childLanes = this.lanes = 0,
        this.alternate = null
    }
    function de(t, e, l, a) {
        return new $h(t,e,l,a)
    }
    function Wi(t) {
        return t = t.prototype,
        !(!t || !t.isReactComponent)
    }
    function Ve(t, e) {
        var l = t.alternate;
        return l === null ? (l = de(t.tag, e, t.key, t.mode),
        l.elementType = t.elementType,
        l.type = t.type,
        l.stateNode = t.stateNode,
        l.alternate = t,
        t.alternate = l) : (l.pendingProps = e,
        l.type = t.type,
        l.flags = 0,
        l.subtreeFlags = 0,
        l.deletions = null),
        l.flags = t.flags & 65011712,
        l.childLanes = t.childLanes,
        l.lanes = t.lanes,
        l.child = t.child,
        l.memoizedProps = t.memoizedProps,
        l.memoizedState = t.memoizedState,
        l.updateQueue = t.updateQueue,
        e = t.dependencies,
        l.dependencies = e === null ? null : {
            lanes: e.lanes,
            firstContext: e.firstContext
        },
        l.sibling = t.sibling,
        l.index = t.index,
        l.ref = t.ref,
        l.refCleanup = t.refCleanup,
        l
    }
    function tr(t, e) {
        t.flags &= 65011714;
        var l = t.alternate;
        return l === null ? (t.childLanes = 0,
        t.lanes = e,
        t.child = null,
        t.subtreeFlags = 0,
        t.memoizedProps = null,
        t.memoizedState = null,
        t.updateQueue = null,
        t.dependencies = null,
        t.stateNode = null) : (t.childLanes = l.childLanes,
        t.lanes = l.lanes,
        t.child = l.child,
        t.subtreeFlags = 0,
        t.deletions = null,
        t.memoizedProps = l.memoizedProps,
        t.memoizedState = l.memoizedState,
        t.updateQueue = l.updateQueue,
        t.type = l.type,
        e = l.dependencies,
        t.dependencies = e === null ? null : {
            lanes: e.lanes,
            firstContext: e.firstContext
        }),
        t
    }
    function ru(t, e, l, a, n, u) {
        var c = 0;
        if (a = t,
        typeof t == "function")
            Wi(t) && (c = 1);
        else if (typeof t == "string")
            c = tg(t, l, Q.current) ? 26 : t === "html" || t === "head" || t === "body" ? 27 : 5;
        else
            t: switch (t) {
            case Tt:
                return t = de(31, l, e, n),
                t.elementType = Tt,
                t.lanes = u,
                t;
            case J:
                return Xl(l.children, n, u, e);
            case X:
                c = 8,
                n |= 24;
                break;
            case Z:
                return t = de(12, l, e, n | 2),
                t.elementType = Z,
                t.lanes = u,
                t;
            case zt:
                return t = de(13, l, e, n),
                t.elementType = zt,
                t.lanes = u,
                t;
            case qt:
                return t = de(19, l, e, n),
                t.elementType = qt,
                t.lanes = u,
                t;
            default:
                if (typeof t == "object" && t !== null)
                    switch (t.$$typeof) {
                    case Y:
                        c = 10;
                        break t;
                    case et:
                        c = 9;
                        break t;
                    case dt:
                        c = 11;
                        break t;
                    case P:
                        c = 14;
                        break t;
                    case Bt:
                        c = 16,
                        a = null;
                        break t
                    }
                c = 29,
                l = Error(f(130, t === null ? "null" : typeof t, "")),
                a = null
            }
        return e = de(c, l, e, n),
        e.elementType = t,
        e.type = a,
        e.lanes = u,
        e
    }
    function Xl(t, e, l, a) {
        return t = de(7, t, a, e),
        t.lanes = l,
        t
    }
    function Fi(t, e, l) {
        return t = de(6, t, null, e),
        t.lanes = l,
        t
    }
    function er(t) {
        var e = de(18, null, null, 0);
        return e.stateNode = t,
        e
    }
    function Ii(t, e, l) {
        return e = de(4, t.children !== null ? t.children : [], t.key, e),
        e.lanes = l,
        e.stateNode = {
            containerInfo: t.containerInfo,
            pendingChildren: null,
            implementation: t.implementation
        },
        e
    }
    var lr = new WeakMap;
    function Se(t, e) {
        if (typeof t == "object" && t !== null) {
            var l = lr.get(t);
            return l !== void 0 ? l : (e = {
                value: t,
                source: e,
                stack: tf(e)
            },
            lr.set(t, e),
            e)
        }
        return {
            value: t,
            source: e,
            stack: tf(e)
        }
    }
    var xa = []
      , ya = 0
      , ou = null
      , nn = 0
      , Ne = []
      , je = 0
      , dl = null
      , Re = 1
      , Ue = "";
    function Ke(t, e) {
        xa[ya++] = nn,
        xa[ya++] = ou,
        ou = t,
        nn = e
    }
    function ar(t, e, l) {
        Ne[je++] = Re,
        Ne[je++] = Ue,
        Ne[je++] = dl,
        dl = t;
        var a = Re;
        t = Ue;
        var n = 32 - re(a) - 1;
        a &= ~(1 << n),
        l += 1;
        var u = 32 - re(e) + n;
        if (30 < u) {
            var c = n - n % 5;
            u = (a & (1 << c) - 1).toString(32),
            a >>= c,
            n -= c,
            Re = 1 << 32 - re(e) + n | l << n | a,
            Ue = u + t
        } else
            Re = 1 << u | l << n | a,
            Ue = t
    }
    function Pi(t) {
        t.return !== null && (Ke(t, 1),
        ar(t, 1, 0))
    }
    function tc(t) {
        for (; t === ou; )
            ou = xa[--ya],
            xa[ya] = null,
            nn = xa[--ya],
            xa[ya] = null;
        for (; t === dl; )
            dl = Ne[--je],
            Ne[je] = null,
            Ue = Ne[--je],
            Ne[je] = null,
            Re = Ne[--je],
            Ne[je] = null
    }
    function nr(t, e) {
        Ne[je++] = Re,
        Ne[je++] = Ue,
        Ne[je++] = dl,
        Re = e.id,
        Ue = e.overflow,
        dl = t
    }
    var Zt = null
      , St = null
      , ct = !1
      , ml = null
      , Ee = !1
      , ec = Error(f(519));
    function hl(t) {
        var e = Error(f(418, 1 < arguments.length && arguments[1] !== void 0 && arguments[1] ? "text" : "HTML", ""));
        throw un(Se(e, t)),
        ec
    }
    function ur(t) {
        var e = t.stateNode
          , l = t.type
          , a = t.memoizedProps;
        switch (e[Qt] = t,
        e[It] = a,
        l) {
        case "dialog":
            nt("cancel", e),
            nt("close", e);
            break;
        case "iframe":
        case "object":
        case "embed":
            nt("load", e);
            break;
        case "video":
        case "audio":
            for (l = 0; l < _n.length; l++)
                nt(_n[l], e);
            break;
        case "source":
            nt("error", e);
            break;
        case "img":
        case "image":
        case "link":
            nt("error", e),
            nt("load", e);
            break;
        case "details":
            nt("toggle", e);
            break;
        case "input":
            nt("invalid", e),
            vf(e, a.value, a.defaultValue, a.checked, a.defaultChecked, a.type, a.name, !0);
            break;
        case "select":
            nt("invalid", e);
            break;
        case "textarea":
            nt("invalid", e),
            bf(e, a.value, a.defaultValue, a.children)
        }
        l = a.children,
        typeof l != "string" && typeof l != "number" && typeof l != "bigint" || e.textContent === "" + l || a.suppressHydrationWarning === !0 || jd(e.textContent, l) ? (a.popover != null && (nt("beforetoggle", e),
        nt("toggle", e)),
        a.onScroll != null && nt("scroll", e),
        a.onScrollEnd != null && nt("scrollend", e),
        a.onClick != null && (e.onclick = Qe),
        e = !0) : e = !1,
        e || hl(t, !0)
    }
    function ir(t) {
        for (Zt = t.return; Zt; )
            switch (Zt.tag) {
            case 5:
            case 31:
            case 13:
                Ee = !1;
                return;
            case 27:
            case 3:
                Ee = !0;
                return;
            default:
                Zt = Zt.return
            }
    }
    function va(t) {
        if (t !== Zt)
            return !1;
        if (!ct)
            return ir(t),
            ct = !0,
            !1;
        var e = t.tag, l;
        if ((l = e !== 3 && e !== 27) && ((l = e === 5) && (l = t.type,
        l = !(l !== "form" && l !== "button") || ps(t.type, t.memoizedProps)),
        l = !l),
        l && St && hl(t),
        ir(t),
        e === 13) {
            if (t = t.memoizedState,
            t = t !== null ? t.dehydrated : null,
            !t)
                throw Error(f(317));
            St = Dd(t)
        } else if (e === 31) {
            if (t = t.memoizedState,
            t = t !== null ? t.dehydrated : null,
            !t)
                throw Error(f(317));
            St = Dd(t)
        } else
            e === 27 ? (e = St,
            _l(t.type) ? (t = Es,
            Es = null,
            St = t) : St = e) : St = Zt ? Te(t.stateNode.nextSibling) : null;
        return !0
    }
    function Ql() {
        St = Zt = null,
        ct = !1
    }
    function lc() {
        var t = ml;
        return t !== null && (ae === null ? ae = t : ae.push.apply(ae, t),
        ml = null),
        t
    }
    function un(t) {
        ml === null ? ml = [t] : ml.push(t)
    }
    var ac = v(null)
      , Zl = null
      , Je = null;
    function gl(t, e, l) {
        B(ac, e._currentValue),
        e._currentValue = l
    }
    function ke(t) {
        t._currentValue = ac.current,
        R(ac)
    }
    function nc(t, e, l) {
        for (; t !== null; ) {
            var a = t.alternate;
            if ((t.childLanes & e) !== e ? (t.childLanes |= e,
            a !== null && (a.childLanes |= e)) : a !== null && (a.childLanes & e) !== e && (a.childLanes |= e),
            t === l)
                break;
            t = t.return
        }
    }
    function uc(t, e, l, a) {
        var n = t.child;
        for (n !== null && (n.return = t); n !== null; ) {
            var u = n.dependencies;
            if (u !== null) {
                var c = n.child;
                u = u.firstContext;
                t: for (; u !== null; ) {
                    var r = u;
                    u = n;
                    for (var h = 0; h < e.length; h++)
                        if (r.context === e[h]) {
                            u.lanes |= l,
                            r = u.alternate,
                            r !== null && (r.lanes |= l),
                            nc(u.return, l, t),
                            a || (c = null);
                            break t
                        }
                    u = r.next
                }
            } else if (n.tag === 18) {
                if (c = n.return,
                c === null)
                    throw Error(f(341));
                c.lanes |= l,
                u = c.alternate,
                u !== null && (u.lanes |= l),
                nc(c, l, t),
                c = null
            } else
                c = n.child;
            if (c !== null)
                c.return = n;
            else
                for (c = n; c !== null; ) {
                    if (c === t) {
                        c = null;
                        break
                    }
                    if (n = c.sibling,
                    n !== null) {
                        n.return = c.return,
                        c = n;
                        break
                    }
                    c = c.return
                }
            n = c
        }
    }
    function pa(t, e, l, a) {
        t = null;
        for (var n = e, u = !1; n !== null; ) {
            if (!u) {
                if ((n.flags & 524288) !== 0)
                    u = !0;
                else if ((n.flags & 262144) !== 0)
                    break
            }
            if (n.tag === 10) {
                var c = n.alternate;
                if (c === null)
                    throw Error(f(387));
                if (c = c.memoizedProps,
                c !== null) {
                    var r = n.type;
                    oe(n.pendingProps.value, c.value) || (t !== null ? t.push(r) : t = [r])
                }
            } else if (n === ot.current) {
                if (c = n.alternate,
                c === null)
                    throw Error(f(387));
                c.memoizedState.memoizedState !== n.memoizedState.memoizedState && (t !== null ? t.push(Cn) : t = [Cn])
            }
            n = n.return
        }
        t !== null && uc(e, t, l, a),
        e.flags |= 262144
    }
    function du(t) {
        for (t = t.firstContext; t !== null; ) {
            if (!oe(t.context._currentValue, t.memoizedValue))
                return !0;
            t = t.next
        }
        return !1
    }
    function Vl(t) {
        Zl = t,
        Je = null,
        t = t.dependencies,
        t !== null && (t.firstContext = null)
    }
    function Vt(t) {
        return cr(Zl, t)
    }
    function mu(t, e) {
        return Zl === null && Vl(t),
        cr(t, e)
    }
    function cr(t, e) {
        var l = e._currentValue;
        if (e = {
            context: e,
            memoizedValue: l,
            next: null
        },
        Je === null) {
            if (t === null)
                throw Error(f(308));
            Je = e,
            t.dependencies = {
                lanes: 0,
                firstContext: e
            },
            t.flags |= 524288
        } else
            Je = Je.next = e;
        return l
    }
    var Wh = typeof AbortController < "u" ? AbortController : function() {
        var t = []
          , e = this.signal = {
            aborted: !1,
            addEventListener: function(l, a) {
                t.push(a)
            }
        };
        this.abort = function() {
            e.aborted = !0,
            t.forEach(function(l) {
                return l()
            })
        }
    }
      , Fh = s.unstable_scheduleCallback
      , Ih = s.unstable_NormalPriority
      , Ct = {
        $$typeof: Y,
        Consumer: null,
        Provider: null,
        _currentValue: null,
        _currentValue2: null,
        _threadCount: 0
    };
    function ic() {
        return {
            controller: new Wh,
            data: new Map,
            refCount: 0
        }
    }
    function cn(t) {
        t.refCount--,
        t.refCount === 0 && Fh(Ih, function() {
            t.controller.abort()
        })
    }
    var sn = null
      , cc = 0
      , ba = 0
      , Sa = null;
    function Ph(t, e) {
        if (sn === null) {
            var l = sn = [];
            cc = 0,
            ba = rs(),
            Sa = {
                status: "pending",
                value: void 0,
                then: function(a) {
                    l.push(a)
                }
            }
        }
        return cc++,
        e.then(sr, sr),
        e
    }
    function sr() {
        if (--cc === 0 && sn !== null) {
            Sa !== null && (Sa.status = "fulfilled");
            var t = sn;
            sn = null,
            ba = 0,
            Sa = null;
            for (var e = 0; e < t.length; e++)
                (0,
                t[e])()
        }
    }
    function t0(t, e) {
        var l = []
          , a = {
            status: "pending",
            value: null,
            reason: null,
            then: function(n) {
                l.push(n)
            }
        };
        return t.then(function() {
            a.status = "fulfilled",
            a.value = e;
            for (var n = 0; n < l.length; n++)
                (0,
                l[n])(e)
        }, function(n) {
            for (a.status = "rejected",
            a.reason = n,
            n = 0; n < l.length; n++)
                (0,
                l[n])(void 0)
        }),
        a
    }
    var fr = w.S;
    w.S = function(t, e) {
        Jo = se(),
        typeof e == "object" && e !== null && typeof e.then == "function" && Ph(t, e),
        fr !== null && fr(t, e)
    }
    ;
    var Kl = v(null);
    function sc() {
        var t = Kl.current;
        return t !== null ? t : bt.pooledCache
    }
    function hu(t, e) {
        e === null ? B(Kl, Kl.current) : B(Kl, e.pool)
    }
    function rr() {
        var t = sc();
        return t === null ? null : {
            parent: Ct._currentValue,
            pool: t
        }
    }
    var Na = Error(f(460))
      , fc = Error(f(474))
      , gu = Error(f(542))
      , xu = {
        then: function() {}
    };
    function or(t) {
        return t = t.status,
        t === "fulfilled" || t === "rejected"
    }
    function dr(t, e, l) {
        switch (l = t[l],
        l === void 0 ? t.push(e) : l !== e && (e.then(Qe, Qe),
        e = l),
        e.status) {
        case "fulfilled":
            return e.value;
        case "rejected":
            throw t = e.reason,
            hr(t),
            t;
        default:
            if (typeof e.status == "string")
                e.then(Qe, Qe);
            else {
                if (t = bt,
                t !== null && 100 < t.shellSuspendCounter)
                    throw Error(f(482));
                t = e,
                t.status = "pending",
                t.then(function(a) {
                    if (e.status === "pending") {
                        var n = e;
                        n.status = "fulfilled",
                        n.value = a
                    }
                }, function(a) {
                    if (e.status === "pending") {
                        var n = e;
                        n.status = "rejected",
                        n.reason = a
                    }
                })
            }
            switch (e.status) {
            case "fulfilled":
                return e.value;
            case "rejected":
                throw t = e.reason,
                hr(t),
                t
            }
            throw kl = e,
            Na
        }
    }
    function Jl(t) {
        try {
            var e = t._init;
            return e(t._payload)
        } catch (l) {
            throw l !== null && typeof l == "object" && typeof l.then == "function" ? (kl = l,
            Na) : l
        }
    }
    var kl = null;
    function mr() {
        if (kl === null)
            throw Error(f(459));
        var t = kl;
        return kl = null,
        t
    }
    function hr(t) {
        if (t === Na || t === gu)
            throw Error(f(483))
    }
    var ja = null
      , fn = 0;
    function yu(t) {
        var e = fn;
        return fn += 1,
        ja === null && (ja = []),
        dr(ja, t, e)
    }
    function rn(t, e) {
        e = e.props.ref,
        t.ref = e !== void 0 ? e : null
    }
    function vu(t, e) {
        throw e.$$typeof === H ? Error(f(525)) : (t = Object.prototype.toString.call(e),
        Error(f(31, t === "[object Object]" ? "object with keys {" + Object.keys(e).join(", ") + "}" : t)))
    }
    function gr(t) {
        function e(b, y) {
            if (t) {
                var j = b.deletions;
                j === null ? (b.deletions = [y],
                b.flags |= 16) : j.push(y)
            }
        }
        function l(b, y) {
            if (!t)
                return null;
            for (; y !== null; )
                e(b, y),
                y = y.sibling;
            return null
        }
        function a(b) {
            for (var y = new Map; b !== null; )
                b.key !== null ? y.set(b.key, b) : y.set(b.index, b),
                b = b.sibling;
            return y
        }
        function n(b, y) {
            return b = Ve(b, y),
            b.index = 0,
            b.sibling = null,
            b
        }
        function u(b, y, j) {
            return b.index = j,
            t ? (j = b.alternate,
            j !== null ? (j = j.index,
            j < y ? (b.flags |= 67108866,
            y) : j) : (b.flags |= 67108866,
            y)) : (b.flags |= 1048576,
            y)
        }
        function c(b) {
            return t && b.alternate === null && (b.flags |= 67108866),
            b
        }
        function r(b, y, j, D) {
            return y === null || y.tag !== 6 ? (y = Fi(j, b.mode, D),
            y.return = b,
            y) : (y = n(y, j),
            y.return = b,
            y)
        }
        function h(b, y, j, D) {
            var K = j.type;
            return K === J ? O(b, y, j.props.children, D, j.key) : y !== null && (y.elementType === K || typeof K == "object" && K !== null && K.$$typeof === Bt && Jl(K) === y.type) ? (y = n(y, j.props),
            rn(y, j),
            y.return = b,
            y) : (y = ru(j.type, j.key, j.props, null, b.mode, D),
            rn(y, j),
            y.return = b,
            y)
        }
        function E(b, y, j, D) {
            return y === null || y.tag !== 4 || y.stateNode.containerInfo !== j.containerInfo || y.stateNode.implementation !== j.implementation ? (y = Ii(j, b.mode, D),
            y.return = b,
            y) : (y = n(y, j.children || []),
            y.return = b,
            y)
        }
        function O(b, y, j, D, K) {
            return y === null || y.tag !== 7 ? (y = Xl(j, b.mode, D, K),
            y.return = b,
            y) : (y = n(y, j),
            y.return = b,
            y)
        }
        function C(b, y, j) {
            if (typeof y == "string" && y !== "" || typeof y == "number" || typeof y == "bigint")
                return y = Fi("" + y, b.mode, j),
                y.return = b,
                y;
            if (typeof y == "object" && y !== null) {
                switch (y.$$typeof) {
                case U:
                    return j = ru(y.type, y.key, y.props, null, b.mode, j),
                    rn(j, y),
                    j.return = b,
                    j;
                case L:
                    return y = Ii(y, b.mode, j),
                    y.return = b,
                    y;
                case Bt:
                    return y = Jl(y),
                    C(b, y, j)
                }
                if (Me(y) || Ft(y))
                    return y = Xl(y, b.mode, j, null),
                    y.return = b,
                    y;
                if (typeof y.then == "function")
                    return C(b, yu(y), j);
                if (y.$$typeof === Y)
                    return C(b, mu(b, y), j);
                vu(b, y)
            }
            return null
        }
        function z(b, y, j, D) {
            var K = y !== null ? y.key : null;
            if (typeof j == "string" && j !== "" || typeof j == "number" || typeof j == "bigint")
                return K !== null ? null : r(b, y, "" + j, D);
            if (typeof j == "object" && j !== null) {
                switch (j.$$typeof) {
                case U:
                    return j.key === K ? h(b, y, j, D) : null;
                case L:
                    return j.key === K ? E(b, y, j, D) : null;
                case Bt:
                    return j = Jl(j),
                    z(b, y, j, D)
                }
                if (Me(j) || Ft(j))
                    return K !== null ? null : O(b, y, j, D, null);
                if (typeof j.then == "function")
                    return z(b, y, yu(j), D);
                if (j.$$typeof === Y)
                    return z(b, y, mu(b, j), D);
                vu(b, j)
            }
            return null
        }
        function A(b, y, j, D, K) {
            if (typeof D == "string" && D !== "" || typeof D == "number" || typeof D == "bigint")
                return b = b.get(j) || null,
                r(y, b, "" + D, K);
            if (typeof D == "object" && D !== null) {
                switch (D.$$typeof) {
                case U:
                    return b = b.get(D.key === null ? j : D.key) || null,
                    h(y, b, D, K);
                case L:
                    return b = b.get(D.key === null ? j : D.key) || null,
                    E(y, b, D, K);
                case Bt:
                    return D = Jl(D),
                    A(b, y, j, D, K)
                }
                if (Me(D) || Ft(D))
                    return b = b.get(j) || null,
                    O(y, b, D, K, null);
                if (typeof D.then == "function")
                    return A(b, y, j, yu(D), K);
                if (D.$$typeof === Y)
                    return A(b, y, j, mu(y, D), K);
                vu(y, D)
            }
            return null
        }
        function G(b, y, j, D) {
            for (var K = null, st = null, V = y, tt = y = 0, it = null; V !== null && tt < j.length; tt++) {
                V.index > tt ? (it = V,
                V = null) : it = V.sibling;
                var ft = z(b, V, j[tt], D);
                if (ft === null) {
                    V === null && (V = it);
                    break
                }
                t && V && ft.alternate === null && e(b, V),
                y = u(ft, y, tt),
                st === null ? K = ft : st.sibling = ft,
                st = ft,
                V = it
            }
            if (tt === j.length)
                return l(b, V),
                ct && Ke(b, tt),
                K;
            if (V === null) {
                for (; tt < j.length; tt++)
                    V = C(b, j[tt], D),
                    V !== null && (y = u(V, y, tt),
                    st === null ? K = V : st.sibling = V,
                    st = V);
                return ct && Ke(b, tt),
                K
            }
            for (V = a(V); tt < j.length; tt++)
                it = A(V, b, tt, j[tt], D),
                it !== null && (t && it.alternate !== null && V.delete(it.key === null ? tt : it.key),
                y = u(it, y, tt),
                st === null ? K = it : st.sibling = it,
                st = it);
            return t && V.forEach(function(Cl) {
                return e(b, Cl)
            }),
            ct && Ke(b, tt),
            K
        }
        function k(b, y, j, D) {
            if (j == null)
                throw Error(f(151));
            for (var K = null, st = null, V = y, tt = y = 0, it = null, ft = j.next(); V !== null && !ft.done; tt++,
            ft = j.next()) {
                V.index > tt ? (it = V,
                V = null) : it = V.sibling;
                var Cl = z(b, V, ft.value, D);
                if (Cl === null) {
                    V === null && (V = it);
                    break
                }
                t && V && Cl.alternate === null && e(b, V),
                y = u(Cl, y, tt),
                st === null ? K = Cl : st.sibling = Cl,
                st = Cl,
                V = it
            }
            if (ft.done)
                return l(b, V),
                ct && Ke(b, tt),
                K;
            if (V === null) {
                for (; !ft.done; tt++,
                ft = j.next())
                    ft = C(b, ft.value, D),
                    ft !== null && (y = u(ft, y, tt),
                    st === null ? K = ft : st.sibling = ft,
                    st = ft);
                return ct && Ke(b, tt),
                K
            }
            for (V = a(V); !ft.done; tt++,
            ft = j.next())
                ft = A(V, b, tt, ft.value, D),
                ft !== null && (t && ft.alternate !== null && V.delete(ft.key === null ? tt : ft.key),
                y = u(ft, y, tt),
                st === null ? K = ft : st.sibling = ft,
                st = ft);
            return t && V.forEach(function(og) {
                return e(b, og)
            }),
            ct && Ke(b, tt),
            K
        }
        function vt(b, y, j, D) {
            if (typeof j == "object" && j !== null && j.type === J && j.key === null && (j = j.props.children),
            typeof j == "object" && j !== null) {
                switch (j.$$typeof) {
                case U:
                    t: {
                        for (var K = j.key; y !== null; ) {
                            if (y.key === K) {
                                if (K = j.type,
                                K === J) {
                                    if (y.tag === 7) {
                                        l(b, y.sibling),
                                        D = n(y, j.props.children),
                                        D.return = b,
                                        b = D;
                                        break t
                                    }
                                } else if (y.elementType === K || typeof K == "object" && K !== null && K.$$typeof === Bt && Jl(K) === y.type) {
                                    l(b, y.sibling),
                                    D = n(y, j.props),
                                    rn(D, j),
                                    D.return = b,
                                    b = D;
                                    break t
                                }
                                l(b, y);
                                break
                            } else
                                e(b, y);
                            y = y.sibling
                        }
                        j.type === J ? (D = Xl(j.props.children, b.mode, D, j.key),
                        D.return = b,
                        b = D) : (D = ru(j.type, j.key, j.props, null, b.mode, D),
                        rn(D, j),
                        D.return = b,
                        b = D)
                    }
                    return c(b);
                case L:
                    t: {
                        for (K = j.key; y !== null; ) {
                            if (y.key === K)
                                if (y.tag === 4 && y.stateNode.containerInfo === j.containerInfo && y.stateNode.implementation === j.implementation) {
                                    l(b, y.sibling),
                                    D = n(y, j.children || []),
                                    D.return = b,
                                    b = D;
                                    break t
                                } else {
                                    l(b, y);
                                    break
                                }
                            else
                                e(b, y);
                            y = y.sibling
                        }
                        D = Ii(j, b.mode, D),
                        D.return = b,
                        b = D
                    }
                    return c(b);
                case Bt:
                    return j = Jl(j),
                    vt(b, y, j, D)
                }
                if (Me(j))
                    return G(b, y, j, D);
                if (Ft(j)) {
                    if (K = Ft(j),
                    typeof K != "function")
                        throw Error(f(150));
                    return j = K.call(j),
                    k(b, y, j, D)
                }
                if (typeof j.then == "function")
                    return vt(b, y, yu(j), D);
                if (j.$$typeof === Y)
                    return vt(b, y, mu(b, j), D);
                vu(b, j)
            }
            return typeof j == "string" && j !== "" || typeof j == "number" || typeof j == "bigint" ? (j = "" + j,
            y !== null && y.tag === 6 ? (l(b, y.sibling),
            D = n(y, j),
            D.return = b,
            b = D) : (l(b, y),
            D = Fi(j, b.mode, D),
            D.return = b,
            b = D),
            c(b)) : l(b, y)
        }
        return function(b, y, j, D) {
            try {
                fn = 0;
                var K = vt(b, y, j, D);
                return ja = null,
                K
            } catch (V) {
                if (V === Na || V === gu)
                    throw V;
                var st = de(29, V, null, b.mode);
                return st.lanes = D,
                st.return = b,
                st
            } finally {}
        }
    }
    var $l = gr(!0)
      , xr = gr(!1)
      , xl = !1;
    function rc(t) {
        t.updateQueue = {
            baseState: t.memoizedState,
            firstBaseUpdate: null,
            lastBaseUpdate: null,
            shared: {
                pending: null,
                lanes: 0,
                hiddenCallbacks: null
            },
            callbacks: null
        }
    }
    function oc(t, e) {
        t = t.updateQueue,
        e.updateQueue === t && (e.updateQueue = {
            baseState: t.baseState,
            firstBaseUpdate: t.firstBaseUpdate,
            lastBaseUpdate: t.lastBaseUpdate,
            shared: t.shared,
            callbacks: null
        })
    }
    function yl(t) {
        return {
            lane: t,
            tag: 0,
            payload: null,
            callback: null,
            next: null
        }
    }
    function vl(t, e, l) {
        var a = t.updateQueue;
        if (a === null)
            return null;
        if (a = a.shared,
        (rt & 2) !== 0) {
            var n = a.pending;
            return n === null ? e.next = e : (e.next = n.next,
            n.next = e),
            a.pending = e,
            e = fu(t),
            Pf(t, null, l),
            e
        }
        return su(t, a, e, l),
        fu(t)
    }
    function on(t, e, l) {
        if (e = e.updateQueue,
        e !== null && (e = e.shared,
        (l & 4194048) !== 0)) {
            var a = e.lanes;
            a &= t.pendingLanes,
            l |= a,
            e.lanes = l,
            cf(t, l)
        }
    }
    function dc(t, e) {
        var l = t.updateQueue
          , a = t.alternate;
        if (a !== null && (a = a.updateQueue,
        l === a)) {
            var n = null
              , u = null;
            if (l = l.firstBaseUpdate,
            l !== null) {
                do {
                    var c = {
                        lane: l.lane,
                        tag: l.tag,
                        payload: l.payload,
                        callback: null,
                        next: null
                    };
                    u === null ? n = u = c : u = u.next = c,
                    l = l.next
                } while (l !== null);
                u === null ? n = u = e : u = u.next = e
            } else
                n = u = e;
            l = {
                baseState: a.baseState,
                firstBaseUpdate: n,
                lastBaseUpdate: u,
                shared: a.shared,
                callbacks: a.callbacks
            },
            t.updateQueue = l;
            return
        }
        t = l.lastBaseUpdate,
        t === null ? l.firstBaseUpdate = e : t.next = e,
        l.lastBaseUpdate = e
    }
    var mc = !1;
    function dn() {
        if (mc) {
            var t = Sa;
            if (t !== null)
                throw t
        }
    }
    function mn(t, e, l, a) {
        mc = !1;
        var n = t.updateQueue;
        xl = !1;
        var u = n.firstBaseUpdate
          , c = n.lastBaseUpdate
          , r = n.shared.pending;
        if (r !== null) {
            n.shared.pending = null;
            var h = r
              , E = h.next;
            h.next = null,
            c === null ? u = E : c.next = E,
            c = h;
            var O = t.alternate;
            O !== null && (O = O.updateQueue,
            r = O.lastBaseUpdate,
            r !== c && (r === null ? O.firstBaseUpdate = E : r.next = E,
            O.lastBaseUpdate = h))
        }
        if (u !== null) {
            var C = n.baseState;
            c = 0,
            O = E = h = null,
            r = u;
            do {
                var z = r.lane & -536870913
                  , A = z !== r.lane;
                if (A ? (ut & z) === z : (a & z) === z) {
                    z !== 0 && z === ba && (mc = !0),
                    O !== null && (O = O.next = {
                        lane: 0,
                        tag: r.tag,
                        payload: r.payload,
                        callback: null,
                        next: null
                    });
                    t: {
                        var G = t
                          , k = r;
                        z = e;
                        var vt = l;
                        switch (k.tag) {
                        case 1:
                            if (G = k.payload,
                            typeof G == "function") {
                                C = G.call(vt, C, z);
                                break t
                            }
                            C = G;
                            break t;
                        case 3:
                            G.flags = G.flags & -65537 | 128;
                        case 0:
                            if (G = k.payload,
                            z = typeof G == "function" ? G.call(vt, C, z) : G,
                            z == null)
                                break t;
                            C = _({}, C, z);
                            break t;
                        case 2:
                            xl = !0
                        }
                    }
                    z = r.callback,
                    z !== null && (t.flags |= 64,
                    A && (t.flags |= 8192),
                    A = n.callbacks,
                    A === null ? n.callbacks = [z] : A.push(z))
                } else
                    A = {
                        lane: z,
                        tag: r.tag,
                        payload: r.payload,
                        callback: r.callback,
                        next: null
                    },
                    O === null ? (E = O = A,
                    h = C) : O = O.next = A,
                    c |= z;
                if (r = r.next,
                r === null) {
                    if (r = n.shared.pending,
                    r === null)
                        break;
                    A = r,
                    r = A.next,
                    A.next = null,
                    n.lastBaseUpdate = A,
                    n.shared.pending = null
                }
            } while (!0);
            O === null && (h = C),
            n.baseState = h,
            n.firstBaseUpdate = E,
            n.lastBaseUpdate = O,
            u === null && (n.shared.lanes = 0),
            jl |= c,
            t.lanes = c,
            t.memoizedState = C
        }
    }
    function yr(t, e) {
        if (typeof t != "function")
            throw Error(f(191, t));
        t.call(e)
    }
    function vr(t, e) {
        var l = t.callbacks;
        if (l !== null)
            for (t.callbacks = null,
            t = 0; t < l.length; t++)
                yr(l[t], e)
    }
    var Ea = v(null)
      , pu = v(0);
    function pr(t, e) {
        t = al,
        B(pu, t),
        B(Ea, e),
        al = t | e.baseLanes
    }
    function hc() {
        B(pu, al),
        B(Ea, Ea.current)
    }
    function gc() {
        al = pu.current,
        R(Ea),
        R(pu)
    }
    var me = v(null)
      , ze = null;
    function pl(t) {
        var e = t.alternate;
        B(wt, wt.current & 1),
        B(me, t),
        ze === null && (e === null || Ea.current !== null || e.memoizedState !== null) && (ze = t)
    }
    function xc(t) {
        B(wt, wt.current),
        B(me, t),
        ze === null && (ze = t)
    }
    function br(t) {
        t.tag === 22 ? (B(wt, wt.current),
        B(me, t),
        ze === null && (ze = t)) : bl()
    }
    function bl() {
        B(wt, wt.current),
        B(me, me.current)
    }
    function he(t) {
        R(me),
        ze === t && (ze = null),
        R(wt)
    }
    var wt = v(0);
    function bu(t) {
        for (var e = t; e !== null; ) {
            if (e.tag === 13) {
                var l = e.memoizedState;
                if (l !== null && (l = l.dehydrated,
                l === null || Ns(l) || js(l)))
                    return e
            } else if (e.tag === 19 && (e.memoizedProps.revealOrder === "forwards" || e.memoizedProps.revealOrder === "backwards" || e.memoizedProps.revealOrder === "unstable_legacy-backwards" || e.memoizedProps.revealOrder === "together")) {
                if ((e.flags & 128) !== 0)
                    return e
            } else if (e.child !== null) {
                e.child.return = e,
                e = e.child;
                continue
            }
            if (e === t)
                break;
            for (; e.sibling === null; ) {
                if (e.return === null || e.return === t)
                    return null;
                e = e.return
            }
            e.sibling.return = e.return,
            e = e.sibling
        }
        return null
    }
    var $e = 0
      , I = null
      , xt = null
      , Rt = null
      , Su = !1
      , za = !1
      , Wl = !1
      , Nu = 0
      , hn = 0
      , Ta = null
      , e0 = 0;
    function At() {
        throw Error(f(321))
    }
    function yc(t, e) {
        if (e === null)
            return !1;
        for (var l = 0; l < e.length && l < t.length; l++)
            if (!oe(t[l], e[l]))
                return !1;
        return !0
    }
    function vc(t, e, l, a, n, u) {
        return $e = u,
        I = e,
        e.memoizedState = null,
        e.updateQueue = null,
        e.lanes = 0,
        w.H = t === null || t.memoizedState === null ? ao : Cc,
        Wl = !1,
        u = l(a, n),
        Wl = !1,
        za && (u = Nr(e, l, a, n)),
        Sr(t),
        u
    }
    function Sr(t) {
        w.H = yn;
        var e = xt !== null && xt.next !== null;
        if ($e = 0,
        Rt = xt = I = null,
        Su = !1,
        hn = 0,
        Ta = null,
        e)
            throw Error(f(300));
        t === null || Ut || (t = t.dependencies,
        t !== null && du(t) && (Ut = !0))
    }
    function Nr(t, e, l, a) {
        I = t;
        var n = 0;
        do {
            if (za && (Ta = null),
            hn = 0,
            za = !1,
            25 <= n)
                throw Error(f(301));
            if (n += 1,
            Rt = xt = null,
            t.updateQueue != null) {
                var u = t.updateQueue;
                u.lastEffect = null,
                u.events = null,
                u.stores = null,
                u.memoCache != null && (u.memoCache.index = 0)
            }
            w.H = no,
            u = e(l, a)
        } while (za);
        return u
    }
    function l0() {
        var t = w.H
          , e = t.useState()[0];
        return e = typeof e.then == "function" ? gn(e) : e,
        t = t.useState()[0],
        (xt !== null ? xt.memoizedState : null) !== t && (I.flags |= 1024),
        e
    }
    function pc() {
        var t = Nu !== 0;
        return Nu = 0,
        t
    }
    function bc(t, e, l) {
        e.updateQueue = t.updateQueue,
        e.flags &= -2053,
        t.lanes &= ~l
    }
    function Sc(t) {
        if (Su) {
            for (t = t.memoizedState; t !== null; ) {
                var e = t.queue;
                e !== null && (e.pending = null),
                t = t.next
            }
            Su = !1
        }
        $e = 0,
        Rt = xt = I = null,
        za = !1,
        hn = Nu = 0,
        Ta = null
    }
    function Wt() {
        var t = {
            memoizedState: null,
            baseState: null,
            baseQueue: null,
            queue: null,
            next: null
        };
        return Rt === null ? I.memoizedState = Rt = t : Rt = Rt.next = t,
        Rt
    }
    function Dt() {
        if (xt === null) {
            var t = I.alternate;
            t = t !== null ? t.memoizedState : null
        } else
            t = xt.next;
        var e = Rt === null ? I.memoizedState : Rt.next;
        if (e !== null)
            Rt = e,
            xt = t;
        else {
            if (t === null)
                throw I.alternate === null ? Error(f(467)) : Error(f(310));
            xt = t,
            t = {
                memoizedState: xt.memoizedState,
                baseState: xt.baseState,
                baseQueue: xt.baseQueue,
                queue: xt.queue,
                next: null
            },
            Rt === null ? I.memoizedState = Rt = t : Rt = Rt.next = t
        }
        return Rt
    }
    function ju() {
        return {
            lastEffect: null,
            events: null,
            stores: null,
            memoCache: null
        }
    }
    function gn(t) {
        var e = hn;
        return hn += 1,
        Ta === null && (Ta = []),
        t = dr(Ta, t, e),
        e = I,
        (Rt === null ? e.memoizedState : Rt.next) === null && (e = e.alternate,
        w.H = e === null || e.memoizedState === null ? ao : Cc),
        t
    }
    function Eu(t) {
        if (t !== null && typeof t == "object") {
            if (typeof t.then == "function")
                return gn(t);
            if (t.$$typeof === Y)
                return Vt(t)
        }
        throw Error(f(438, String(t)))
    }
    function Nc(t) {
        var e = null
          , l = I.updateQueue;
        if (l !== null && (e = l.memoCache),
        e == null) {
            var a = I.alternate;
            a !== null && (a = a.updateQueue,
            a !== null && (a = a.memoCache,
            a != null && (e = {
                data: a.data.map(function(n) {
                    return n.slice()
                }),
                index: 0
            })))
        }
        if (e == null && (e = {
            data: [],
            index: 0
        }),
        l === null && (l = ju(),
        I.updateQueue = l),
        l.memoCache = e,
        l = e.data[e.index],
        l === void 0)
            for (l = e.data[e.index] = Array(t),
            a = 0; a < t; a++)
                l[a] = ie;
        return e.index++,
        l
    }
    function We(t, e) {
        return typeof e == "function" ? e(t) : e
    }
    function zu(t) {
        var e = Dt();
        return jc(e, xt, t)
    }
    function jc(t, e, l) {
        var a = t.queue;
        if (a === null)
            throw Error(f(311));
        a.lastRenderedReducer = l;
        var n = t.baseQueue
          , u = a.pending;
        if (u !== null) {
            if (n !== null) {
                var c = n.next;
                n.next = u.next,
                u.next = c
            }
            e.baseQueue = n = u,
            a.pending = null
        }
        if (u = t.baseState,
        n === null)
            t.memoizedState = u;
        else {
            e = n.next;
            var r = c = null
              , h = null
              , E = e
              , O = !1;
            do {
                var C = E.lane & -536870913;
                if (C !== E.lane ? (ut & C) === C : ($e & C) === C) {
                    var z = E.revertLane;
                    if (z === 0)
                        h !== null && (h = h.next = {
                            lane: 0,
                            revertLane: 0,
                            gesture: null,
                            action: E.action,
                            hasEagerState: E.hasEagerState,
                            eagerState: E.eagerState,
                            next: null
                        }),
                        C === ba && (O = !0);
                    else if (($e & z) === z) {
                        E = E.next,
                        z === ba && (O = !0);
                        continue
                    } else
                        C = {
                            lane: 0,
                            revertLane: E.revertLane,
                            gesture: null,
                            action: E.action,
                            hasEagerState: E.hasEagerState,
                            eagerState: E.eagerState,
                            next: null
                        },
                        h === null ? (r = h = C,
                        c = u) : h = h.next = C,
                        I.lanes |= z,
                        jl |= z;
                    C = E.action,
                    Wl && l(u, C),
                    u = E.hasEagerState ? E.eagerState : l(u, C)
                } else
                    z = {
                        lane: C,
                        revertLane: E.revertLane,
                        gesture: E.gesture,
                        action: E.action,
                        hasEagerState: E.hasEagerState,
                        eagerState: E.eagerState,
                        next: null
                    },
                    h === null ? (r = h = z,
                    c = u) : h = h.next = z,
                    I.lanes |= C,
                    jl |= C;
                E = E.next
            } while (E !== null && E !== e);
            if (h === null ? c = u : h.next = r,
            !oe(u, t.memoizedState) && (Ut = !0,
            O && (l = Sa,
            l !== null)))
                throw l;
            t.memoizedState = u,
            t.baseState = c,
            t.baseQueue = h,
            a.lastRenderedState = u
        }
        return n === null && (a.lanes = 0),
        [t.memoizedState, a.dispatch]
    }
    function Ec(t) {
        var e = Dt()
          , l = e.queue;
        if (l === null)
            throw Error(f(311));
        l.lastRenderedReducer = t;
        var a = l.dispatch
          , n = l.pending
          , u = e.memoizedState;
        if (n !== null) {
            l.pending = null;
            var c = n = n.next;
            do
                u = t(u, c.action),
                c = c.next;
            while (c !== n);
            oe(u, e.memoizedState) || (Ut = !0),
            e.memoizedState = u,
            e.baseQueue === null && (e.baseState = u),
            l.lastRenderedState = u
        }
        return [u, a]
    }
    function jr(t, e, l) {
        var a = I
          , n = Dt()
          , u = ct;
        if (u) {
            if (l === void 0)
                throw Error(f(407));
            l = l()
        } else
            l = e();
        var c = !oe((xt || n).memoizedState, l);
        if (c && (n.memoizedState = l,
        Ut = !0),
        n = n.queue,
        Ac(Tr.bind(null, a, n, t), [t]),
        n.getSnapshot !== e || c || Rt !== null && Rt.memoizedState.tag & 1) {
            if (a.flags |= 2048,
            Aa(9, {
                destroy: void 0
            }, zr.bind(null, a, n, l, e), null),
            bt === null)
                throw Error(f(349));
            u || ($e & 127) !== 0 || Er(a, e, l)
        }
        return l
    }
    function Er(t, e, l) {
        t.flags |= 16384,
        t = {
            getSnapshot: e,
            value: l
        },
        e = I.updateQueue,
        e === null ? (e = ju(),
        I.updateQueue = e,
        e.stores = [t]) : (l = e.stores,
        l === null ? e.stores = [t] : l.push(t))
    }
    function zr(t, e, l, a) {
        e.value = l,
        e.getSnapshot = a,
        Ar(e) && _r(t)
    }
    function Tr(t, e, l) {
        return l(function() {
            Ar(e) && _r(t)
        })
    }
    function Ar(t) {
        var e = t.getSnapshot;
        t = t.value;
        try {
            var l = e();
            return !oe(t, l)
        } catch {
            return !0
        }
    }
    function _r(t) {
        var e = Gl(t, 2);
        e !== null && ne(e, t, 2)
    }
    function zc(t) {
        var e = Wt();
        if (typeof t == "function") {
            var l = t;
            if (t = l(),
            Wl) {
                fl(!0);
                try {
                    l()
                } finally {
                    fl(!1)
                }
            }
        }
        return e.memoizedState = e.baseState = t,
        e.queue = {
            pending: null,
            lanes: 0,
            dispatch: null,
            lastRenderedReducer: We,
            lastRenderedState: t
        },
        e
    }
    function Mr(t, e, l, a) {
        return t.baseState = l,
        jc(t, xt, typeof a == "function" ? a : We)
    }
    function a0(t, e, l, a, n) {
        if (_u(t))
            throw Error(f(485));
        if (t = e.action,
        t !== null) {
            var u = {
                payload: n,
                action: t,
                next: null,
                isTransition: !0,
                status: "pending",
                value: null,
                reason: null,
                listeners: [],
                then: function(c) {
                    u.listeners.push(c)
                }
            };
            w.T !== null ? l(!0) : u.isTransition = !1,
            a(u),
            l = e.pending,
            l === null ? (u.next = e.pending = u,
            Or(e, u)) : (u.next = l.next,
            e.pending = l.next = u)
        }
    }
    function Or(t, e) {
        var l = e.action
          , a = e.payload
          , n = t.state;
        if (e.isTransition) {
            var u = w.T
              , c = {};
            w.T = c;
            try {
                var r = l(n, a)
                  , h = w.S;
                h !== null && h(c, r),
                wr(t, e, r)
            } catch (E) {
                Tc(t, e, E)
            } finally {
                u !== null && c.types !== null && (u.types = c.types),
                w.T = u
            }
        } else
            try {
                u = l(n, a),
                wr(t, e, u)
            } catch (E) {
                Tc(t, e, E)
            }
    }
    function wr(t, e, l) {
        l !== null && typeof l == "object" && typeof l.then == "function" ? l.then(function(a) {
            Dr(t, e, a)
        }, function(a) {
            return Tc(t, e, a)
        }) : Dr(t, e, l)
    }
    function Dr(t, e, l) {
        e.status = "fulfilled",
        e.value = l,
        Cr(e),
        t.state = l,
        e = t.pending,
        e !== null && (l = e.next,
        l === e ? t.pending = null : (l = l.next,
        e.next = l,
        Or(t, l)))
    }
    function Tc(t, e, l) {
        var a = t.pending;
        if (t.pending = null,
        a !== null) {
            a = a.next;
            do
                e.status = "rejected",
                e.reason = l,
                Cr(e),
                e = e.next;
            while (e !== a)
        }
        t.action = null
    }
    function Cr(t) {
        t = t.listeners;
        for (var e = 0; e < t.length; e++)
            (0,
            t[e])()
    }
    function Rr(t, e) {
        return e
    }
    function Ur(t, e) {
        if (ct) {
            var l = bt.formState;
            if (l !== null) {
                t: {
                    var a = I;
                    if (ct) {
                        if (St) {
                            e: {
                                for (var n = St, u = Ee; n.nodeType !== 8; ) {
                                    if (!u) {
                                        n = null;
                                        break e
                                    }
                                    if (n = Te(n.nextSibling),
                                    n === null) {
                                        n = null;
                                        break e
                                    }
                                }
                                u = n.data,
                                n = u === "F!" || u === "F" ? n : null
                            }
                            if (n) {
                                St = Te(n.nextSibling),
                                a = n.data === "F!";
                                break t
                            }
                        }
                        hl(a)
                    }
                    a = !1
                }
                a && (e = l[0])
            }
        }
        return l = Wt(),
        l.memoizedState = l.baseState = e,
        a = {
            pending: null,
            lanes: 0,
            dispatch: null,
            lastRenderedReducer: Rr,
            lastRenderedState: e
        },
        l.queue = a,
        l = to.bind(null, I, a),
        a.dispatch = l,
        a = zc(!1),
        u = Dc.bind(null, I, !1, a.queue),
        a = Wt(),
        n = {
            state: e,
            dispatch: null,
            action: t,
            pending: null
        },
        a.queue = n,
        l = a0.bind(null, I, n, u, l),
        n.dispatch = l,
        a.memoizedState = t,
        [e, l, !1]
    }
    function Hr(t) {
        var e = Dt();
        return qr(e, xt, t)
    }
    function qr(t, e, l) {
        if (e = jc(t, e, Rr)[0],
        t = zu(We)[0],
        typeof e == "object" && e !== null && typeof e.then == "function")
            try {
                var a = gn(e)
            } catch (c) {
                throw c === Na ? gu : c
            }
        else
            a = e;
        e = Dt();
        var n = e.queue
          , u = n.dispatch;
        return l !== e.memoizedState && (I.flags |= 2048,
        Aa(9, {
            destroy: void 0
        }, n0.bind(null, n, l), null)),
        [a, u, t]
    }
    function n0(t, e) {
        t.action = e
    }
    function Br(t) {
        var e = Dt()
          , l = xt;
        if (l !== null)
            return qr(e, l, t);
        Dt(),
        e = e.memoizedState,
        l = Dt();
        var a = l.queue.dispatch;
        return l.memoizedState = t,
        [e, a, !1]
    }
    function Aa(t, e, l, a) {
        return t = {
            tag: t,
            create: l,
            deps: a,
            inst: e,
            next: null
        },
        e = I.updateQueue,
        e === null && (e = ju(),
        I.updateQueue = e),
        l = e.lastEffect,
        l === null ? e.lastEffect = t.next = t : (a = l.next,
        l.next = t,
        t.next = a,
        e.lastEffect = t),
        t
    }
    function Yr() {
        return Dt().memoizedState
    }
    function Tu(t, e, l, a) {
        var n = Wt();
        I.flags |= t,
        n.memoizedState = Aa(1 | e, {
            destroy: void 0
        }, l, a === void 0 ? null : a)
    }
    function Au(t, e, l, a) {
        var n = Dt();
        a = a === void 0 ? null : a;
        var u = n.memoizedState.inst;
        xt !== null && a !== null && yc(a, xt.memoizedState.deps) ? n.memoizedState = Aa(e, u, l, a) : (I.flags |= t,
        n.memoizedState = Aa(1 | e, u, l, a))
    }
    function Lr(t, e) {
        Tu(8390656, 8, t, e)
    }
    function Ac(t, e) {
        Au(2048, 8, t, e)
    }
    function u0(t) {
        I.flags |= 4;
        var e = I.updateQueue;
        if (e === null)
            e = ju(),
            I.updateQueue = e,
            e.events = [t];
        else {
            var l = e.events;
            l === null ? e.events = [t] : l.push(t)
        }
    }
    function Gr(t) {
        var e = Dt().memoizedState;
        return u0({
            ref: e,
            nextImpl: t
        }),
        function() {
            if ((rt & 2) !== 0)
                throw Error(f(440));
            return e.impl.apply(void 0, arguments)
        }
    }
    function Xr(t, e) {
        return Au(4, 2, t, e)
    }
    function Qr(t, e) {
        return Au(4, 4, t, e)
    }
    function Zr(t, e) {
        if (typeof e == "function") {
            t = t();
            var l = e(t);
            return function() {
                typeof l == "function" ? l() : e(null)
            }
        }
        if (e != null)
            return t = t(),
            e.current = t,
            function() {
                e.current = null
            }
    }
    function Vr(t, e, l) {
        l = l != null ? l.concat([t]) : null,
        Au(4, 4, Zr.bind(null, e, t), l)
    }
    function _c() {}
    function Kr(t, e) {
        var l = Dt();
        e = e === void 0 ? null : e;
        var a = l.memoizedState;
        return e !== null && yc(e, a[1]) ? a[0] : (l.memoizedState = [t, e],
        t)
    }
    function Jr(t, e) {
        var l = Dt();
        e = e === void 0 ? null : e;
        var a = l.memoizedState;
        if (e !== null && yc(e, a[1]))
            return a[0];
        if (a = t(),
        Wl) {
            fl(!0);
            try {
                t()
            } finally {
                fl(!1)
            }
        }
        return l.memoizedState = [a, e],
        a
    }
    function Mc(t, e, l) {
        return l === void 0 || ($e & 1073741824) !== 0 && (ut & 261930) === 0 ? t.memoizedState = e : (t.memoizedState = l,
        t = $o(),
        I.lanes |= t,
        jl |= t,
        l)
    }
    function kr(t, e, l, a) {
        return oe(l, e) ? l : Ea.current !== null ? (t = Mc(t, l, a),
        oe(t, e) || (Ut = !0),
        t) : ($e & 42) === 0 || ($e & 1073741824) !== 0 && (ut & 261930) === 0 ? (Ut = !0,
        t.memoizedState = l) : (t = $o(),
        I.lanes |= t,
        jl |= t,
        e)
    }
    function $r(t, e, l, a, n) {
        var u = q.p;
        q.p = u !== 0 && 8 > u ? u : 8;
        var c = w.T
          , r = {};
        w.T = r,
        Dc(t, !1, e, l);
        try {
            var h = n()
              , E = w.S;
            if (E !== null && E(r, h),
            h !== null && typeof h == "object" && typeof h.then == "function") {
                var O = t0(h, a);
                xn(t, e, O, ye(t))
            } else
                xn(t, e, a, ye(t))
        } catch (C) {
            xn(t, e, {
                then: function() {},
                status: "rejected",
                reason: C
            }, ye())
        } finally {
            q.p = u,
            c !== null && r.types !== null && (c.types = r.types),
            w.T = c
        }
    }
    function i0() {}
    function Oc(t, e, l, a) {
        if (t.tag !== 5)
            throw Error(f(476));
        var n = Wr(t).queue;
        $r(t, n, e, $, l === null ? i0 : function() {
            return Fr(t),
            l(a)
        }
        )
    }
    function Wr(t) {
        var e = t.memoizedState;
        if (e !== null)
            return e;
        e = {
            memoizedState: $,
            baseState: $,
            baseQueue: null,
            queue: {
                pending: null,
                lanes: 0,
                dispatch: null,
                lastRenderedReducer: We,
                lastRenderedState: $
            },
            next: null
        };
        var l = {};
        return e.next = {
            memoizedState: l,
            baseState: l,
            baseQueue: null,
            queue: {
                pending: null,
                lanes: 0,
                dispatch: null,
                lastRenderedReducer: We,
                lastRenderedState: l
            },
            next: null
        },
        t.memoizedState = e,
        t = t.alternate,
        t !== null && (t.memoizedState = e),
        e
    }
    function Fr(t) {
        var e = Wr(t);
        e.next === null && (e = t.alternate.memoizedState),
        xn(t, e.next.queue, {}, ye())
    }
    function wc() {
        return Vt(Cn)
    }
    function Ir() {
        return Dt().memoizedState
    }
    function Pr() {
        return Dt().memoizedState
    }
    function c0(t) {
        for (var e = t.return; e !== null; ) {
            switch (e.tag) {
            case 24:
            case 3:
                var l = ye();
                t = yl(l);
                var a = vl(e, t, l);
                a !== null && (ne(a, e, l),
                on(a, e, l)),
                e = {
                    cache: ic()
                },
                t.payload = e;
                return
            }
            e = e.return
        }
    }
    function s0(t, e, l) {
        var a = ye();
        l = {
            lane: a,
            revertLane: 0,
            gesture: null,
            action: l,
            hasEagerState: !1,
            eagerState: null,
            next: null
        },
        _u(t) ? eo(e, l) : (l = $i(t, e, l, a),
        l !== null && (ne(l, t, a),
        lo(l, e, a)))
    }
    function to(t, e, l) {
        var a = ye();
        xn(t, e, l, a)
    }
    function xn(t, e, l, a) {
        var n = {
            lane: a,
            revertLane: 0,
            gesture: null,
            action: l,
            hasEagerState: !1,
            eagerState: null,
            next: null
        };
        if (_u(t))
            eo(e, n);
        else {
            var u = t.alternate;
            if (t.lanes === 0 && (u === null || u.lanes === 0) && (u = e.lastRenderedReducer,
            u !== null))
                try {
                    var c = e.lastRenderedState
                      , r = u(c, l);
                    if (n.hasEagerState = !0,
                    n.eagerState = r,
                    oe(r, c))
                        return su(t, e, n, 0),
                        bt === null && cu(),
                        !1
                } catch {} finally {}
            if (l = $i(t, e, n, a),
            l !== null)
                return ne(l, t, a),
                lo(l, e, a),
                !0
        }
        return !1
    }
    function Dc(t, e, l, a) {
        if (a = {
            lane: 2,
            revertLane: rs(),
            gesture: null,
            action: a,
            hasEagerState: !1,
            eagerState: null,
            next: null
        },
        _u(t)) {
            if (e)
                throw Error(f(479))
        } else
            e = $i(t, l, a, 2),
            e !== null && ne(e, t, 2)
    }
    function _u(t) {
        var e = t.alternate;
        return t === I || e !== null && e === I
    }
    function eo(t, e) {
        za = Su = !0;
        var l = t.pending;
        l === null ? e.next = e : (e.next = l.next,
        l.next = e),
        t.pending = e
    }
    function lo(t, e, l) {
        if ((l & 4194048) !== 0) {
            var a = e.lanes;
            a &= t.pendingLanes,
            l |= a,
            e.lanes = l,
            cf(t, l)
        }
    }
    var yn = {
        readContext: Vt,
        use: Eu,
        useCallback: At,
        useContext: At,
        useEffect: At,
        useImperativeHandle: At,
        useLayoutEffect: At,
        useInsertionEffect: At,
        useMemo: At,
        useReducer: At,
        useRef: At,
        useState: At,
        useDebugValue: At,
        useDeferredValue: At,
        useTransition: At,
        useSyncExternalStore: At,
        useId: At,
        useHostTransitionStatus: At,
        useFormState: At,
        useActionState: At,
        useOptimistic: At,
        useMemoCache: At,
        useCacheRefresh: At
    };
    yn.useEffectEvent = At;
    var ao = {
        readContext: Vt,
        use: Eu,
        useCallback: function(t, e) {
            return Wt().memoizedState = [t, e === void 0 ? null : e],
            t
        },
        useContext: Vt,
        useEffect: Lr,
        useImperativeHandle: function(t, e, l) {
            l = l != null ? l.concat([t]) : null,
            Tu(4194308, 4, Zr.bind(null, e, t), l)
        },
        useLayoutEffect: function(t, e) {
            return Tu(4194308, 4, t, e)
        },
        useInsertionEffect: function(t, e) {
            Tu(4, 2, t, e)
        },
        useMemo: function(t, e) {
            var l = Wt();
            e = e === void 0 ? null : e;
            var a = t();
            if (Wl) {
                fl(!0);
                try {
                    t()
                } finally {
                    fl(!1)
                }
            }
            return l.memoizedState = [a, e],
            a
        },
        useReducer: function(t, e, l) {
            var a = Wt();
            if (l !== void 0) {
                var n = l(e);
                if (Wl) {
                    fl(!0);
                    try {
                        l(e)
                    } finally {
                        fl(!1)
                    }
                }
            } else
                n = e;
            return a.memoizedState = a.baseState = n,
            t = {
                pending: null,
                lanes: 0,
                dispatch: null,
                lastRenderedReducer: t,
                lastRenderedState: n
            },
            a.queue = t,
            t = t.dispatch = s0.bind(null, I, t),
            [a.memoizedState, t]
        },
        useRef: function(t) {
            var e = Wt();
            return t = {
                current: t
            },
            e.memoizedState = t
        },
        useState: function(t) {
            t = zc(t);
            var e = t.queue
              , l = to.bind(null, I, e);
            return e.dispatch = l,
            [t.memoizedState, l]
        },
        useDebugValue: _c,
        useDeferredValue: function(t, e) {
            var l = Wt();
            return Mc(l, t, e)
        },
        useTransition: function() {
            var t = zc(!1);
            return t = $r.bind(null, I, t.queue, !0, !1),
            Wt().memoizedState = t,
            [!1, t]
        },
        useSyncExternalStore: function(t, e, l) {
            var a = I
              , n = Wt();
            if (ct) {
                if (l === void 0)
                    throw Error(f(407));
                l = l()
            } else {
                if (l = e(),
                bt === null)
                    throw Error(f(349));
                (ut & 127) !== 0 || Er(a, e, l)
            }
            n.memoizedState = l;
            var u = {
                value: l,
                getSnapshot: e
            };
            return n.queue = u,
            Lr(Tr.bind(null, a, u, t), [t]),
            a.flags |= 2048,
            Aa(9, {
                destroy: void 0
            }, zr.bind(null, a, u, l, e), null),
            l
        },
        useId: function() {
            var t = Wt()
              , e = bt.identifierPrefix;
            if (ct) {
                var l = Ue
                  , a = Re;
                l = (a & ~(1 << 32 - re(a) - 1)).toString(32) + l,
                e = "_" + e + "R_" + l,
                l = Nu++,
                0 < l && (e += "H" + l.toString(32)),
                e += "_"
            } else
                l = e0++,
                e = "_" + e + "r_" + l.toString(32) + "_";
            return t.memoizedState = e
        },
        useHostTransitionStatus: wc,
        useFormState: Ur,
        useActionState: Ur,
        useOptimistic: function(t) {
            var e = Wt();
            e.memoizedState = e.baseState = t;
            var l = {
                pending: null,
                lanes: 0,
                dispatch: null,
                lastRenderedReducer: null,
                lastRenderedState: null
            };
            return e.queue = l,
            e = Dc.bind(null, I, !0, l),
            l.dispatch = e,
            [t, e]
        },
        useMemoCache: Nc,
        useCacheRefresh: function() {
            return Wt().memoizedState = c0.bind(null, I)
        },
        useEffectEvent: function(t) {
            var e = Wt()
              , l = {
                impl: t
            };
            return e.memoizedState = l,
            function() {
                if ((rt & 2) !== 0)
                    throw Error(f(440));
                return l.impl.apply(void 0, arguments)
            }
        }
    }
      , Cc = {
        readContext: Vt,
        use: Eu,
        useCallback: Kr,
        useContext: Vt,
        useEffect: Ac,
        useImperativeHandle: Vr,
        useInsertionEffect: Xr,
        useLayoutEffect: Qr,
        useMemo: Jr,
        useReducer: zu,
        useRef: Yr,
        useState: function() {
            return zu(We)
        },
        useDebugValue: _c,
        useDeferredValue: function(t, e) {
            var l = Dt();
            return kr(l, xt.memoizedState, t, e)
        },
        useTransition: function() {
            var t = zu(We)[0]
              , e = Dt().memoizedState;
            return [typeof t == "boolean" ? t : gn(t), e]
        },
        useSyncExternalStore: jr,
        useId: Ir,
        useHostTransitionStatus: wc,
        useFormState: Hr,
        useActionState: Hr,
        useOptimistic: function(t, e) {
            var l = Dt();
            return Mr(l, xt, t, e)
        },
        useMemoCache: Nc,
        useCacheRefresh: Pr
    };
    Cc.useEffectEvent = Gr;
    var no = {
        readContext: Vt,
        use: Eu,
        useCallback: Kr,
        useContext: Vt,
        useEffect: Ac,
        useImperativeHandle: Vr,
        useInsertionEffect: Xr,
        useLayoutEffect: Qr,
        useMemo: Jr,
        useReducer: Ec,
        useRef: Yr,
        useState: function() {
            return Ec(We)
        },
        useDebugValue: _c,
        useDeferredValue: function(t, e) {
            var l = Dt();
            return xt === null ? Mc(l, t, e) : kr(l, xt.memoizedState, t, e)
        },
        useTransition: function() {
            var t = Ec(We)[0]
              , e = Dt().memoizedState;
            return [typeof t == "boolean" ? t : gn(t), e]
        },
        useSyncExternalStore: jr,
        useId: Ir,
        useHostTransitionStatus: wc,
        useFormState: Br,
        useActionState: Br,
        useOptimistic: function(t, e) {
            var l = Dt();
            return xt !== null ? Mr(l, xt, t, e) : (l.baseState = t,
            [t, l.queue.dispatch])
        },
        useMemoCache: Nc,
        useCacheRefresh: Pr
    };
    no.useEffectEvent = Gr;
    function Rc(t, e, l, a) {
        e = t.memoizedState,
        l = l(a, e),
        l = l == null ? e : _({}, e, l),
        t.memoizedState = l,
        t.lanes === 0 && (t.updateQueue.baseState = l)
    }
    var Uc = {
        enqueueSetState: function(t, e, l) {
            t = t._reactInternals;
            var a = ye()
              , n = yl(a);
            n.payload = e,
            l != null && (n.callback = l),
            e = vl(t, n, a),
            e !== null && (ne(e, t, a),
            on(e, t, a))
        },
        enqueueReplaceState: function(t, e, l) {
            t = t._reactInternals;
            var a = ye()
              , n = yl(a);
            n.tag = 1,
            n.payload = e,
            l != null && (n.callback = l),
            e = vl(t, n, a),
            e !== null && (ne(e, t, a),
            on(e, t, a))
        },
        enqueueForceUpdate: function(t, e) {
            t = t._reactInternals;
            var l = ye()
              , a = yl(l);
            a.tag = 2,
            e != null && (a.callback = e),
            e = vl(t, a, l),
            e !== null && (ne(e, t, l),
            on(e, t, l))
        }
    };
    function uo(t, e, l, a, n, u, c) {
        return t = t.stateNode,
        typeof t.shouldComponentUpdate == "function" ? t.shouldComponentUpdate(a, u, c) : e.prototype && e.prototype.isPureReactComponent ? !ln(l, a) || !ln(n, u) : !0
    }
    function io(t, e, l, a) {
        t = e.state,
        typeof e.componentWillReceiveProps == "function" && e.componentWillReceiveProps(l, a),
        typeof e.UNSAFE_componentWillReceiveProps == "function" && e.UNSAFE_componentWillReceiveProps(l, a),
        e.state !== t && Uc.enqueueReplaceState(e, e.state, null)
    }
    function Fl(t, e) {
        var l = e;
        if ("ref"in e) {
            l = {};
            for (var a in e)
                a !== "ref" && (l[a] = e[a])
        }
        if (t = t.defaultProps) {
            l === e && (l = _({}, l));
            for (var n in t)
                l[n] === void 0 && (l[n] = t[n])
        }
        return l
    }
    function co(t) {
        iu(t)
    }
    function so(t) {
        console.error(t)
    }
    function fo(t) {
        iu(t)
    }
    function Mu(t, e) {
        try {
            var l = t.onUncaughtError;
            l(e.value, {
                componentStack: e.stack
            })
        } catch (a) {
            setTimeout(function() {
                throw a
            })
        }
    }
    function ro(t, e, l) {
        try {
            var a = t.onCaughtError;
            a(l.value, {
                componentStack: l.stack,
                errorBoundary: e.tag === 1 ? e.stateNode : null
            })
        } catch (n) {
            setTimeout(function() {
                throw n
            })
        }
    }
    function Hc(t, e, l) {
        return l = yl(l),
        l.tag = 3,
        l.payload = {
            element: null
        },
        l.callback = function() {
            Mu(t, e)
        }
        ,
        l
    }
    function oo(t) {
        return t = yl(t),
        t.tag = 3,
        t
    }
    function mo(t, e, l, a) {
        var n = l.type.getDerivedStateFromError;
        if (typeof n == "function") {
            var u = a.value;
            t.payload = function() {
                return n(u)
            }
            ,
            t.callback = function() {
                ro(e, l, a)
            }
        }
        var c = l.stateNode;
        c !== null && typeof c.componentDidCatch == "function" && (t.callback = function() {
            ro(e, l, a),
            typeof n != "function" && (El === null ? El = new Set([this]) : El.add(this));
            var r = a.stack;
            this.componentDidCatch(a.value, {
                componentStack: r !== null ? r : ""
            })
        }
        )
    }
    function f0(t, e, l, a, n) {
        if (l.flags |= 32768,
        a !== null && typeof a == "object" && typeof a.then == "function") {
            if (e = l.alternate,
            e !== null && pa(e, l, n, !0),
            l = me.current,
            l !== null) {
                switch (l.tag) {
                case 31:
                case 13:
                    return ze === null ? Gu() : l.alternate === null && _t === 0 && (_t = 3),
                    l.flags &= -257,
                    l.flags |= 65536,
                    l.lanes = n,
                    a === xu ? l.flags |= 16384 : (e = l.updateQueue,
                    e === null ? l.updateQueue = new Set([a]) : e.add(a),
                    cs(t, a, n)),
                    !1;
                case 22:
                    return l.flags |= 65536,
                    a === xu ? l.flags |= 16384 : (e = l.updateQueue,
                    e === null ? (e = {
                        transitions: null,
                        markerInstances: null,
                        retryQueue: new Set([a])
                    },
                    l.updateQueue = e) : (l = e.retryQueue,
                    l === null ? e.retryQueue = new Set([a]) : l.add(a)),
                    cs(t, a, n)),
                    !1
                }
                throw Error(f(435, l.tag))
            }
            return cs(t, a, n),
            Gu(),
            !1
        }
        if (ct)
            return e = me.current,
            e !== null ? ((e.flags & 65536) === 0 && (e.flags |= 256),
            e.flags |= 65536,
            e.lanes = n,
            a !== ec && (t = Error(f(422), {
                cause: a
            }),
            un(Se(t, l)))) : (a !== ec && (e = Error(f(423), {
                cause: a
            }),
            un(Se(e, l))),
            t = t.current.alternate,
            t.flags |= 65536,
            n &= -n,
            t.lanes |= n,
            a = Se(a, l),
            n = Hc(t.stateNode, a, n),
            dc(t, n),
            _t !== 4 && (_t = 2)),
            !1;
        var u = Error(f(520), {
            cause: a
        });
        if (u = Se(u, l),
        zn === null ? zn = [u] : zn.push(u),
        _t !== 4 && (_t = 2),
        e === null)
            return !0;
        a = Se(a, l),
        l = e;
        do {
            switch (l.tag) {
            case 3:
                return l.flags |= 65536,
                t = n & -n,
                l.lanes |= t,
                t = Hc(l.stateNode, a, t),
                dc(l, t),
                !1;
            case 1:
                if (e = l.type,
                u = l.stateNode,
                (l.flags & 128) === 0 && (typeof e.getDerivedStateFromError == "function" || u !== null && typeof u.componentDidCatch == "function" && (El === null || !El.has(u))))
                    return l.flags |= 65536,
                    n &= -n,
                    l.lanes |= n,
                    n = oo(n),
                    mo(n, t, l, a),
                    dc(l, n),
                    !1
            }
            l = l.return
        } while (l !== null);
        return !1
    }
    var qc = Error(f(461))
      , Ut = !1;
    function Kt(t, e, l, a) {
        e.child = t === null ? xr(e, null, l, a) : $l(e, t.child, l, a)
    }
    function ho(t, e, l, a, n) {
        l = l.render;
        var u = e.ref;
        if ("ref"in a) {
            var c = {};
            for (var r in a)
                r !== "ref" && (c[r] = a[r])
        } else
            c = a;
        return Vl(e),
        a = vc(t, e, l, c, u, n),
        r = pc(),
        t !== null && !Ut ? (bc(t, e, n),
        Fe(t, e, n)) : (ct && r && Pi(e),
        e.flags |= 1,
        Kt(t, e, a, n),
        e.child)
    }
    function go(t, e, l, a, n) {
        if (t === null) {
            var u = l.type;
            return typeof u == "function" && !Wi(u) && u.defaultProps === void 0 && l.compare === null ? (e.tag = 15,
            e.type = u,
            xo(t, e, u, a, n)) : (t = ru(l.type, null, a, e, e.mode, n),
            t.ref = e.ref,
            t.return = e,
            e.child = t)
        }
        if (u = t.child,
        !Vc(t, n)) {
            var c = u.memoizedProps;
            if (l = l.compare,
            l = l !== null ? l : ln,
            l(c, a) && t.ref === e.ref)
                return Fe(t, e, n)
        }
        return e.flags |= 1,
        t = Ve(u, a),
        t.ref = e.ref,
        t.return = e,
        e.child = t
    }
    function xo(t, e, l, a, n) {
        if (t !== null) {
            var u = t.memoizedProps;
            if (ln(u, a) && t.ref === e.ref)
                if (Ut = !1,
                e.pendingProps = a = u,
                Vc(t, n))
                    (t.flags & 131072) !== 0 && (Ut = !0);
                else
                    return e.lanes = t.lanes,
                    Fe(t, e, n)
        }
        return Bc(t, e, l, a, n)
    }
    function yo(t, e, l, a) {
        var n = a.children
          , u = t !== null ? t.memoizedState : null;
        if (t === null && e.stateNode === null && (e.stateNode = {
            _visibility: 1,
            _pendingMarkers: null,
            _retryCache: null,
            _transitions: null
        }),
        a.mode === "hidden") {
            if ((e.flags & 128) !== 0) {
                if (u = u !== null ? u.baseLanes | l : l,
                t !== null) {
                    for (a = e.child = t.child,
                    n = 0; a !== null; )
                        n = n | a.lanes | a.childLanes,
                        a = a.sibling;
                    a = n & ~u
                } else
                    a = 0,
                    e.child = null;
                return vo(t, e, u, l, a)
            }
            if ((l & 536870912) !== 0)
                e.memoizedState = {
                    baseLanes: 0,
                    cachePool: null
                },
                t !== null && hu(e, u !== null ? u.cachePool : null),
                u !== null ? pr(e, u) : hc(),
                br(e);
            else
                return a = e.lanes = 536870912,
                vo(t, e, u !== null ? u.baseLanes | l : l, l, a)
        } else
            u !== null ? (hu(e, u.cachePool),
            pr(e, u),
            bl(),
            e.memoizedState = null) : (t !== null && hu(e, null),
            hc(),
            bl());
        return Kt(t, e, n, l),
        e.child
    }
    function vn(t, e) {
        return t !== null && t.tag === 22 || e.stateNode !== null || (e.stateNode = {
            _visibility: 1,
            _pendingMarkers: null,
            _retryCache: null,
            _transitions: null
        }),
        e.sibling
    }
    function vo(t, e, l, a, n) {
        var u = sc();
        return u = u === null ? null : {
            parent: Ct._currentValue,
            pool: u
        },
        e.memoizedState = {
            baseLanes: l,
            cachePool: u
        },
        t !== null && hu(e, null),
        hc(),
        br(e),
        t !== null && pa(t, e, a, !0),
        e.childLanes = n,
        null
    }
    function Ou(t, e) {
        return e = Du({
            mode: e.mode,
            children: e.children
        }, t.mode),
        e.ref = t.ref,
        t.child = e,
        e.return = t,
        e
    }
    function po(t, e, l) {
        return $l(e, t.child, null, l),
        t = Ou(e, e.pendingProps),
        t.flags |= 2,
        he(e),
        e.memoizedState = null,
        t
    }
    function r0(t, e, l) {
        var a = e.pendingProps
          , n = (e.flags & 128) !== 0;
        if (e.flags &= -129,
        t === null) {
            if (ct) {
                if (a.mode === "hidden")
                    return t = Ou(e, a),
                    e.lanes = 536870912,
                    vn(null, t);
                if (xc(e),
                (t = St) ? (t = wd(t, Ee),
                t = t !== null && t.data === "&" ? t : null,
                t !== null && (e.memoizedState = {
                    dehydrated: t,
                    treeContext: dl !== null ? {
                        id: Re,
                        overflow: Ue
                    } : null,
                    retryLane: 536870912,
                    hydrationErrors: null
                },
                l = er(t),
                l.return = e,
                e.child = l,
                Zt = e,
                St = null)) : t = null,
                t === null)
                    throw hl(e);
                return e.lanes = 536870912,
                null
            }
            return Ou(e, a)
        }
        var u = t.memoizedState;
        if (u !== null) {
            var c = u.dehydrated;
            if (xc(e),
            n)
                if (e.flags & 256)
                    e.flags &= -257,
                    e = po(t, e, l);
                else if (e.memoizedState !== null)
                    e.child = t.child,
                    e.flags |= 128,
                    e = null;
                else
                    throw Error(f(558));
            else if (Ut || pa(t, e, l, !1),
            n = (l & t.childLanes) !== 0,
            Ut || n) {
                if (a = bt,
                a !== null && (c = sf(a, l),
                c !== 0 && c !== u.retryLane))
                    throw u.retryLane = c,
                    Gl(t, c),
                    ne(a, t, c),
                    qc;
                Gu(),
                e = po(t, e, l)
            } else
                t = u.treeContext,
                St = Te(c.nextSibling),
                Zt = e,
                ct = !0,
                ml = null,
                Ee = !1,
                t !== null && nr(e, t),
                e = Ou(e, a),
                e.flags |= 4096;
            return e
        }
        return t = Ve(t.child, {
            mode: a.mode,
            children: a.children
        }),
        t.ref = e.ref,
        e.child = t,
        t.return = e,
        t
    }
    function wu(t, e) {
        var l = e.ref;
        if (l === null)
            t !== null && t.ref !== null && (e.flags |= 4194816);
        else {
            if (typeof l != "function" && typeof l != "object")
                throw Error(f(284));
            (t === null || t.ref !== l) && (e.flags |= 4194816)
        }
    }
    function Bc(t, e, l, a, n) {
        return Vl(e),
        l = vc(t, e, l, a, void 0, n),
        a = pc(),
        t !== null && !Ut ? (bc(t, e, n),
        Fe(t, e, n)) : (ct && a && Pi(e),
        e.flags |= 1,
        Kt(t, e, l, n),
        e.child)
    }
    function bo(t, e, l, a, n, u) {
        return Vl(e),
        e.updateQueue = null,
        l = Nr(e, a, l, n),
        Sr(t),
        a = pc(),
        t !== null && !Ut ? (bc(t, e, u),
        Fe(t, e, u)) : (ct && a && Pi(e),
        e.flags |= 1,
        Kt(t, e, l, u),
        e.child)
    }
    function So(t, e, l, a, n) {
        if (Vl(e),
        e.stateNode === null) {
            var u = ga
              , c = l.contextType;
            typeof c == "object" && c !== null && (u = Vt(c)),
            u = new l(a,u),
            e.memoizedState = u.state !== null && u.state !== void 0 ? u.state : null,
            u.updater = Uc,
            e.stateNode = u,
            u._reactInternals = e,
            u = e.stateNode,
            u.props = a,
            u.state = e.memoizedState,
            u.refs = {},
            rc(e),
            c = l.contextType,
            u.context = typeof c == "object" && c !== null ? Vt(c) : ga,
            u.state = e.memoizedState,
            c = l.getDerivedStateFromProps,
            typeof c == "function" && (Rc(e, l, c, a),
            u.state = e.memoizedState),
            typeof l.getDerivedStateFromProps == "function" || typeof u.getSnapshotBeforeUpdate == "function" || typeof u.UNSAFE_componentWillMount != "function" && typeof u.componentWillMount != "function" || (c = u.state,
            typeof u.componentWillMount == "function" && u.componentWillMount(),
            typeof u.UNSAFE_componentWillMount == "function" && u.UNSAFE_componentWillMount(),
            c !== u.state && Uc.enqueueReplaceState(u, u.state, null),
            mn(e, a, u, n),
            dn(),
            u.state = e.memoizedState),
            typeof u.componentDidMount == "function" && (e.flags |= 4194308),
            a = !0
        } else if (t === null) {
            u = e.stateNode;
            var r = e.memoizedProps
              , h = Fl(l, r);
            u.props = h;
            var E = u.context
              , O = l.contextType;
            c = ga,
            typeof O == "object" && O !== null && (c = Vt(O));
            var C = l.getDerivedStateFromProps;
            O = typeof C == "function" || typeof u.getSnapshotBeforeUpdate == "function",
            r = e.pendingProps !== r,
            O || typeof u.UNSAFE_componentWillReceiveProps != "function" && typeof u.componentWillReceiveProps != "function" || (r || E !== c) && io(e, u, a, c),
            xl = !1;
            var z = e.memoizedState;
            u.state = z,
            mn(e, a, u, n),
            dn(),
            E = e.memoizedState,
            r || z !== E || xl ? (typeof C == "function" && (Rc(e, l, C, a),
            E = e.memoizedState),
            (h = xl || uo(e, l, h, a, z, E, c)) ? (O || typeof u.UNSAFE_componentWillMount != "function" && typeof u.componentWillMount != "function" || (typeof u.componentWillMount == "function" && u.componentWillMount(),
            typeof u.UNSAFE_componentWillMount == "function" && u.UNSAFE_componentWillMount()),
            typeof u.componentDidMount == "function" && (e.flags |= 4194308)) : (typeof u.componentDidMount == "function" && (e.flags |= 4194308),
            e.memoizedProps = a,
            e.memoizedState = E),
            u.props = a,
            u.state = E,
            u.context = c,
            a = h) : (typeof u.componentDidMount == "function" && (e.flags |= 4194308),
            a = !1)
        } else {
            u = e.stateNode,
            oc(t, e),
            c = e.memoizedProps,
            O = Fl(l, c),
            u.props = O,
            C = e.pendingProps,
            z = u.context,
            E = l.contextType,
            h = ga,
            typeof E == "object" && E !== null && (h = Vt(E)),
            r = l.getDerivedStateFromProps,
            (E = typeof r == "function" || typeof u.getSnapshotBeforeUpdate == "function") || typeof u.UNSAFE_componentWillReceiveProps != "function" && typeof u.componentWillReceiveProps != "function" || (c !== C || z !== h) && io(e, u, a, h),
            xl = !1,
            z = e.memoizedState,
            u.state = z,
            mn(e, a, u, n),
            dn();
            var A = e.memoizedState;
            c !== C || z !== A || xl || t !== null && t.dependencies !== null && du(t.dependencies) ? (typeof r == "function" && (Rc(e, l, r, a),
            A = e.memoizedState),
            (O = xl || uo(e, l, O, a, z, A, h) || t !== null && t.dependencies !== null && du(t.dependencies)) ? (E || typeof u.UNSAFE_componentWillUpdate != "function" && typeof u.componentWillUpdate != "function" || (typeof u.componentWillUpdate == "function" && u.componentWillUpdate(a, A, h),
            typeof u.UNSAFE_componentWillUpdate == "function" && u.UNSAFE_componentWillUpdate(a, A, h)),
            typeof u.componentDidUpdate == "function" && (e.flags |= 4),
            typeof u.getSnapshotBeforeUpdate == "function" && (e.flags |= 1024)) : (typeof u.componentDidUpdate != "function" || c === t.memoizedProps && z === t.memoizedState || (e.flags |= 4),
            typeof u.getSnapshotBeforeUpdate != "function" || c === t.memoizedProps && z === t.memoizedState || (e.flags |= 1024),
            e.memoizedProps = a,
            e.memoizedState = A),
            u.props = a,
            u.state = A,
            u.context = h,
            a = O) : (typeof u.componentDidUpdate != "function" || c === t.memoizedProps && z === t.memoizedState || (e.flags |= 4),
            typeof u.getSnapshotBeforeUpdate != "function" || c === t.memoizedProps && z === t.memoizedState || (e.flags |= 1024),
            a = !1)
        }
        return u = a,
        wu(t, e),
        a = (e.flags & 128) !== 0,
        u || a ? (u = e.stateNode,
        l = a && typeof l.getDerivedStateFromError != "function" ? null : u.render(),
        e.flags |= 1,
        t !== null && a ? (e.child = $l(e, t.child, null, n),
        e.child = $l(e, null, l, n)) : Kt(t, e, l, n),
        e.memoizedState = u.state,
        t = e.child) : t = Fe(t, e, n),
        t
    }
    function No(t, e, l, a) {
        return Ql(),
        e.flags |= 256,
        Kt(t, e, l, a),
        e.child
    }
    var Yc = {
        dehydrated: null,
        treeContext: null,
        retryLane: 0,
        hydrationErrors: null
    };
    function Lc(t) {
        return {
            baseLanes: t,
            cachePool: rr()
        }
    }
    function Gc(t, e, l) {
        return t = t !== null ? t.childLanes & ~l : 0,
        e && (t |= xe),
        t
    }
    function jo(t, e, l) {
        var a = e.pendingProps, n = !1, u = (e.flags & 128) !== 0, c;
        if ((c = u) || (c = t !== null && t.memoizedState === null ? !1 : (wt.current & 2) !== 0),
        c && (n = !0,
        e.flags &= -129),
        c = (e.flags & 32) !== 0,
        e.flags &= -33,
        t === null) {
            if (ct) {
                if (n ? pl(e) : bl(),
                (t = St) ? (t = wd(t, Ee),
                t = t !== null && t.data !== "&" ? t : null,
                t !== null && (e.memoizedState = {
                    dehydrated: t,
                    treeContext: dl !== null ? {
                        id: Re,
                        overflow: Ue
                    } : null,
                    retryLane: 536870912,
                    hydrationErrors: null
                },
                l = er(t),
                l.return = e,
                e.child = l,
                Zt = e,
                St = null)) : t = null,
                t === null)
                    throw hl(e);
                return js(t) ? e.lanes = 32 : e.lanes = 536870912,
                null
            }
            var r = a.children;
            return a = a.fallback,
            n ? (bl(),
            n = e.mode,
            r = Du({
                mode: "hidden",
                children: r
            }, n),
            a = Xl(a, n, l, null),
            r.return = e,
            a.return = e,
            r.sibling = a,
            e.child = r,
            a = e.child,
            a.memoizedState = Lc(l),
            a.childLanes = Gc(t, c, l),
            e.memoizedState = Yc,
            vn(null, a)) : (pl(e),
            Xc(e, r))
        }
        var h = t.memoizedState;
        if (h !== null && (r = h.dehydrated,
        r !== null)) {
            if (u)
                e.flags & 256 ? (pl(e),
                e.flags &= -257,
                e = Qc(t, e, l)) : e.memoizedState !== null ? (bl(),
                e.child = t.child,
                e.flags |= 128,
                e = null) : (bl(),
                r = a.fallback,
                n = e.mode,
                a = Du({
                    mode: "visible",
                    children: a.children
                }, n),
                r = Xl(r, n, l, null),
                r.flags |= 2,
                a.return = e,
                r.return = e,
                a.sibling = r,
                e.child = a,
                $l(e, t.child, null, l),
                a = e.child,
                a.memoizedState = Lc(l),
                a.childLanes = Gc(t, c, l),
                e.memoizedState = Yc,
                e = vn(null, a));
            else if (pl(e),
            js(r)) {
                if (c = r.nextSibling && r.nextSibling.dataset,
                c)
                    var E = c.dgst;
                c = E,
                a = Error(f(419)),
                a.stack = "",
                a.digest = c,
                un({
                    value: a,
                    source: null,
                    stack: null
                }),
                e = Qc(t, e, l)
            } else if (Ut || pa(t, e, l, !1),
            c = (l & t.childLanes) !== 0,
            Ut || c) {
                if (c = bt,
                c !== null && (a = sf(c, l),
                a !== 0 && a !== h.retryLane))
                    throw h.retryLane = a,
                    Gl(t, a),
                    ne(c, t, a),
                    qc;
                Ns(r) || Gu(),
                e = Qc(t, e, l)
            } else
                Ns(r) ? (e.flags |= 192,
                e.child = t.child,
                e = null) : (t = h.treeContext,
                St = Te(r.nextSibling),
                Zt = e,
                ct = !0,
                ml = null,
                Ee = !1,
                t !== null && nr(e, t),
                e = Xc(e, a.children),
                e.flags |= 4096);
            return e
        }
        return n ? (bl(),
        r = a.fallback,
        n = e.mode,
        h = t.child,
        E = h.sibling,
        a = Ve(h, {
            mode: "hidden",
            children: a.children
        }),
        a.subtreeFlags = h.subtreeFlags & 65011712,
        E !== null ? r = Ve(E, r) : (r = Xl(r, n, l, null),
        r.flags |= 2),
        r.return = e,
        a.return = e,
        a.sibling = r,
        e.child = a,
        vn(null, a),
        a = e.child,
        r = t.child.memoizedState,
        r === null ? r = Lc(l) : (n = r.cachePool,
        n !== null ? (h = Ct._currentValue,
        n = n.parent !== h ? {
            parent: h,
            pool: h
        } : n) : n = rr(),
        r = {
            baseLanes: r.baseLanes | l,
            cachePool: n
        }),
        a.memoizedState = r,
        a.childLanes = Gc(t, c, l),
        e.memoizedState = Yc,
        vn(t.child, a)) : (pl(e),
        l = t.child,
        t = l.sibling,
        l = Ve(l, {
            mode: "visible",
            children: a.children
        }),
        l.return = e,
        l.sibling = null,
        t !== null && (c = e.deletions,
        c === null ? (e.deletions = [t],
        e.flags |= 16) : c.push(t)),
        e.child = l,
        e.memoizedState = null,
        l)
    }
    function Xc(t, e) {
        return e = Du({
            mode: "visible",
            children: e
        }, t.mode),
        e.return = t,
        t.child = e
    }
    function Du(t, e) {
        return t = de(22, t, null, e),
        t.lanes = 0,
        t
    }
    function Qc(t, e, l) {
        return $l(e, t.child, null, l),
        t = Xc(e, e.pendingProps.children),
        t.flags |= 2,
        e.memoizedState = null,
        t
    }
    function Eo(t, e, l) {
        t.lanes |= e;
        var a = t.alternate;
        a !== null && (a.lanes |= e),
        nc(t.return, e, l)
    }
    function Zc(t, e, l, a, n, u) {
        var c = t.memoizedState;
        c === null ? t.memoizedState = {
            isBackwards: e,
            rendering: null,
            renderingStartTime: 0,
            last: a,
            tail: l,
            tailMode: n,
            treeForkCount: u
        } : (c.isBackwards = e,
        c.rendering = null,
        c.renderingStartTime = 0,
        c.last = a,
        c.tail = l,
        c.tailMode = n,
        c.treeForkCount = u)
    }
    function zo(t, e, l) {
        var a = e.pendingProps
          , n = a.revealOrder
          , u = a.tail;
        a = a.children;
        var c = wt.current
          , r = (c & 2) !== 0;
        if (r ? (c = c & 1 | 2,
        e.flags |= 128) : c &= 1,
        B(wt, c),
        Kt(t, e, a, l),
        a = ct ? nn : 0,
        !r && t !== null && (t.flags & 128) !== 0)
            t: for (t = e.child; t !== null; ) {
                if (t.tag === 13)
                    t.memoizedState !== null && Eo(t, l, e);
                else if (t.tag === 19)
                    Eo(t, l, e);
                else if (t.child !== null) {
                    t.child.return = t,
                    t = t.child;
                    continue
                }
                if (t === e)
                    break t;
                for (; t.sibling === null; ) {
                    if (t.return === null || t.return === e)
                        break t;
                    t = t.return
                }
                t.sibling.return = t.return,
                t = t.sibling
            }
        switch (n) {
        case "forwards":
            for (l = e.child,
            n = null; l !== null; )
                t = l.alternate,
                t !== null && bu(t) === null && (n = l),
                l = l.sibling;
            l = n,
            l === null ? (n = e.child,
            e.child = null) : (n = l.sibling,
            l.sibling = null),
            Zc(e, !1, n, l, u, a);
            break;
        case "backwards":
        case "unstable_legacy-backwards":
            for (l = null,
            n = e.child,
            e.child = null; n !== null; ) {
                if (t = n.alternate,
                t !== null && bu(t) === null) {
                    e.child = n;
                    break
                }
                t = n.sibling,
                n.sibling = l,
                l = n,
                n = t
            }
            Zc(e, !0, l, null, u, a);
            break;
        case "together":
            Zc(e, !1, null, null, void 0, a);
            break;
        default:
            e.memoizedState = null
        }
        return e.child
    }
    function Fe(t, e, l) {
        if (t !== null && (e.dependencies = t.dependencies),
        jl |= e.lanes,
        (l & e.childLanes) === 0)
            if (t !== null) {
                if (pa(t, e, l, !1),
                (l & e.childLanes) === 0)
                    return null
            } else
                return null;
        if (t !== null && e.child !== t.child)
            throw Error(f(153));
        if (e.child !== null) {
            for (t = e.child,
            l = Ve(t, t.pendingProps),
            e.child = l,
            l.return = e; t.sibling !== null; )
                t = t.sibling,
                l = l.sibling = Ve(t, t.pendingProps),
                l.return = e;
            l.sibling = null
        }
        return e.child
    }
    function Vc(t, e) {
        return (t.lanes & e) !== 0 ? !0 : (t = t.dependencies,
        !!(t !== null && du(t)))
    }
    function o0(t, e, l) {
        switch (e.tag) {
        case 3:
            $t(e, e.stateNode.containerInfo),
            gl(e, Ct, t.memoizedState.cache),
            Ql();
            break;
        case 27:
        case 5:
            Qa(e);
            break;
        case 4:
            $t(e, e.stateNode.containerInfo);
            break;
        case 10:
            gl(e, e.type, e.memoizedProps.value);
            break;
        case 31:
            if (e.memoizedState !== null)
                return e.flags |= 128,
                xc(e),
                null;
            break;
        case 13:
            var a = e.memoizedState;
            if (a !== null)
                return a.dehydrated !== null ? (pl(e),
                e.flags |= 128,
                null) : (l & e.child.childLanes) !== 0 ? jo(t, e, l) : (pl(e),
                t = Fe(t, e, l),
                t !== null ? t.sibling : null);
            pl(e);
            break;
        case 19:
            var n = (t.flags & 128) !== 0;
            if (a = (l & e.childLanes) !== 0,
            a || (pa(t, e, l, !1),
            a = (l & e.childLanes) !== 0),
            n) {
                if (a)
                    return zo(t, e, l);
                e.flags |= 128
            }
            if (n = e.memoizedState,
            n !== null && (n.rendering = null,
            n.tail = null,
            n.lastEffect = null),
            B(wt, wt.current),
            a)
                break;
            return null;
        case 22:
            return e.lanes = 0,
            yo(t, e, l, e.pendingProps);
        case 24:
            gl(e, Ct, t.memoizedState.cache)
        }
        return Fe(t, e, l)
    }
    function To(t, e, l) {
        if (t !== null)
            if (t.memoizedProps !== e.pendingProps)
                Ut = !0;
            else {
                if (!Vc(t, l) && (e.flags & 128) === 0)
                    return Ut = !1,
                    o0(t, e, l);
                Ut = (t.flags & 131072) !== 0
            }
        else
            Ut = !1,
            ct && (e.flags & 1048576) !== 0 && ar(e, nn, e.index);
        switch (e.lanes = 0,
        e.tag) {
        case 16:
            t: {
                var a = e.pendingProps;
                if (t = Jl(e.elementType),
                e.type = t,
                typeof t == "function")
                    Wi(t) ? (a = Fl(t, a),
                    e.tag = 1,
                    e = So(null, e, t, a, l)) : (e.tag = 0,
                    e = Bc(null, e, t, a, l));
                else {
                    if (t != null) {
                        var n = t.$$typeof;
                        if (n === dt) {
                            e.tag = 11,
                            e = ho(null, e, t, a, l);
                            break t
                        } else if (n === P) {
                            e.tag = 14,
                            e = go(null, e, t, a, l);
                            break t
                        }
                    }
                    throw e = Ge(t) || t,
                    Error(f(306, e, ""))
                }
            }
            return e;
        case 0:
            return Bc(t, e, e.type, e.pendingProps, l);
        case 1:
            return a = e.type,
            n = Fl(a, e.pendingProps),
            So(t, e, a, n, l);
        case 3:
            t: {
                if ($t(e, e.stateNode.containerInfo),
                t === null)
                    throw Error(f(387));
                a = e.pendingProps;
                var u = e.memoizedState;
                n = u.element,
                oc(t, e),
                mn(e, a, null, l);
                var c = e.memoizedState;
                if (a = c.cache,
                gl(e, Ct, a),
                a !== u.cache && uc(e, [Ct], l, !0),
                dn(),
                a = c.element,
                u.isDehydrated)
                    if (u = {
                        element: a,
                        isDehydrated: !1,
                        cache: c.cache
                    },
                    e.updateQueue.baseState = u,
                    e.memoizedState = u,
                    e.flags & 256) {
                        e = No(t, e, a, l);
                        break t
                    } else if (a !== n) {
                        n = Se(Error(f(424)), e),
                        un(n),
                        e = No(t, e, a, l);
                        break t
                    } else {
                        switch (t = e.stateNode.containerInfo,
                        t.nodeType) {
                        case 9:
                            t = t.body;
                            break;
                        default:
                            t = t.nodeName === "HTML" ? t.ownerDocument.body : t
                        }
                        for (St = Te(t.firstChild),
                        Zt = e,
                        ct = !0,
                        ml = null,
                        Ee = !0,
                        l = xr(e, null, a, l),
                        e.child = l; l; )
                            l.flags = l.flags & -3 | 4096,
                            l = l.sibling
                    }
                else {
                    if (Ql(),
                    a === n) {
                        e = Fe(t, e, l);
                        break t
                    }
                    Kt(t, e, a, l)
                }
                e = e.child
            }
            return e;
        case 26:
            return wu(t, e),
            t === null ? (l = qd(e.type, null, e.pendingProps, null)) ? e.memoizedState = l : ct || (l = e.type,
            t = e.pendingProps,
            a = ku(lt.current).createElement(l),
            a[Qt] = e,
            a[It] = t,
            Jt(a, l, t),
            Gt(a),
            e.stateNode = a) : e.memoizedState = qd(e.type, t.memoizedProps, e.pendingProps, t.memoizedState),
            null;
        case 27:
            return Qa(e),
            t === null && ct && (a = e.stateNode = Rd(e.type, e.pendingProps, lt.current),
            Zt = e,
            Ee = !0,
            n = St,
            _l(e.type) ? (Es = n,
            St = Te(a.firstChild)) : St = n),
            Kt(t, e, e.pendingProps.children, l),
            wu(t, e),
            t === null && (e.flags |= 4194304),
            e.child;
        case 5:
            return t === null && ct && ((n = a = St) && (a = G0(a, e.type, e.pendingProps, Ee),
            a !== null ? (e.stateNode = a,
            Zt = e,
            St = Te(a.firstChild),
            Ee = !1,
            n = !0) : n = !1),
            n || hl(e)),
            Qa(e),
            n = e.type,
            u = e.pendingProps,
            c = t !== null ? t.memoizedProps : null,
            a = u.children,
            ps(n, u) ? a = null : c !== null && ps(n, c) && (e.flags |= 32),
            e.memoizedState !== null && (n = vc(t, e, l0, null, null, l),
            Cn._currentValue = n),
            wu(t, e),
            Kt(t, e, a, l),
            e.child;
        case 6:
            return t === null && ct && ((t = l = St) && (l = X0(l, e.pendingProps, Ee),
            l !== null ? (e.stateNode = l,
            Zt = e,
            St = null,
            t = !0) : t = !1),
            t || hl(e)),
            null;
        case 13:
            return jo(t, e, l);
        case 4:
            return $t(e, e.stateNode.containerInfo),
            a = e.pendingProps,
            t === null ? e.child = $l(e, null, a, l) : Kt(t, e, a, l),
            e.child;
        case 11:
            return ho(t, e, e.type, e.pendingProps, l);
        case 7:
            return Kt(t, e, e.pendingProps, l),
            e.child;
        case 8:
            return Kt(t, e, e.pendingProps.children, l),
            e.child;
        case 12:
            return Kt(t, e, e.pendingProps.children, l),
            e.child;
        case 10:
            return a = e.pendingProps,
            gl(e, e.type, a.value),
            Kt(t, e, a.children, l),
            e.child;
        case 9:
            return n = e.type._context,
            a = e.pendingProps.children,
            Vl(e),
            n = Vt(n),
            a = a(n),
            e.flags |= 1,
            Kt(t, e, a, l),
            e.child;
        case 14:
            return go(t, e, e.type, e.pendingProps, l);
        case 15:
            return xo(t, e, e.type, e.pendingProps, l);
        case 19:
            return zo(t, e, l);
        case 31:
            return r0(t, e, l);
        case 22:
            return yo(t, e, l, e.pendingProps);
        case 24:
            return Vl(e),
            a = Vt(Ct),
            t === null ? (n = sc(),
            n === null && (n = bt,
            u = ic(),
            n.pooledCache = u,
            u.refCount++,
            u !== null && (n.pooledCacheLanes |= l),
            n = u),
            e.memoizedState = {
                parent: a,
                cache: n
            },
            rc(e),
            gl(e, Ct, n)) : ((t.lanes & l) !== 0 && (oc(t, e),
            mn(e, null, null, l),
            dn()),
            n = t.memoizedState,
            u = e.memoizedState,
            n.parent !== a ? (n = {
                parent: a,
                cache: a
            },
            e.memoizedState = n,
            e.lanes === 0 && (e.memoizedState = e.updateQueue.baseState = n),
            gl(e, Ct, a)) : (a = u.cache,
            gl(e, Ct, a),
            a !== n.cache && uc(e, [Ct], l, !0))),
            Kt(t, e, e.pendingProps.children, l),
            e.child;
        case 29:
            throw e.pendingProps
        }
        throw Error(f(156, e.tag))
    }
    function Ie(t) {
        t.flags |= 4
    }
    function Kc(t, e, l, a, n) {
        if ((e = (t.mode & 32) !== 0) && (e = !1),
        e) {
            if (t.flags |= 16777216,
            (n & 335544128) === n)
                if (t.stateNode.complete)
                    t.flags |= 8192;
                else if (Po())
                    t.flags |= 8192;
                else
                    throw kl = xu,
                    fc
        } else
            t.flags &= -16777217
    }
    function Ao(t, e) {
        if (e.type !== "stylesheet" || (e.state.loading & 4) !== 0)
            t.flags &= -16777217;
        else if (t.flags |= 16777216,
        !Xd(e))
            if (Po())
                t.flags |= 8192;
            else
                throw kl = xu,
                fc
    }
    function Cu(t, e) {
        e !== null && (t.flags |= 4),
        t.flags & 16384 && (e = t.tag !== 22 ? nf() : 536870912,
        t.lanes |= e,
        wa |= e)
    }
    function pn(t, e) {
        if (!ct)
            switch (t.tailMode) {
            case "hidden":
                e = t.tail;
                for (var l = null; e !== null; )
                    e.alternate !== null && (l = e),
                    e = e.sibling;
                l === null ? t.tail = null : l.sibling = null;
                break;
            case "collapsed":
                l = t.tail;
                for (var a = null; l !== null; )
                    l.alternate !== null && (a = l),
                    l = l.sibling;
                a === null ? e || t.tail === null ? t.tail = null : t.tail.sibling = null : a.sibling = null
            }
    }
    function Nt(t) {
        var e = t.alternate !== null && t.alternate.child === t.child
          , l = 0
          , a = 0;
        if (e)
            for (var n = t.child; n !== null; )
                l |= n.lanes | n.childLanes,
                a |= n.subtreeFlags & 65011712,
                a |= n.flags & 65011712,
                n.return = t,
                n = n.sibling;
        else
            for (n = t.child; n !== null; )
                l |= n.lanes | n.childLanes,
                a |= n.subtreeFlags,
                a |= n.flags,
                n.return = t,
                n = n.sibling;
        return t.subtreeFlags |= a,
        t.childLanes = l,
        e
    }
    function d0(t, e, l) {
        var a = e.pendingProps;
        switch (tc(e),
        e.tag) {
        case 16:
        case 15:
        case 0:
        case 11:
        case 7:
        case 8:
        case 12:
        case 9:
        case 14:
            return Nt(e),
            null;
        case 1:
            return Nt(e),
            null;
        case 3:
            return l = e.stateNode,
            a = null,
            t !== null && (a = t.memoizedState.cache),
            e.memoizedState.cache !== a && (e.flags |= 2048),
            ke(Ct),
            Ot(),
            l.pendingContext && (l.context = l.pendingContext,
            l.pendingContext = null),
            (t === null || t.child === null) && (va(e) ? Ie(e) : t === null || t.memoizedState.isDehydrated && (e.flags & 256) === 0 || (e.flags |= 1024,
            lc())),
            Nt(e),
            null;
        case 26:
            var n = e.type
              , u = e.memoizedState;
            return t === null ? (Ie(e),
            u !== null ? (Nt(e),
            Ao(e, u)) : (Nt(e),
            Kc(e, n, null, a, l))) : u ? u !== t.memoizedState ? (Ie(e),
            Nt(e),
            Ao(e, u)) : (Nt(e),
            e.flags &= -16777217) : (t = t.memoizedProps,
            t !== a && Ie(e),
            Nt(e),
            Kc(e, n, t, a, l)),
            null;
        case 27:
            if (Zn(e),
            l = lt.current,
            n = e.type,
            t !== null && e.stateNode != null)
                t.memoizedProps !== a && Ie(e);
            else {
                if (!a) {
                    if (e.stateNode === null)
                        throw Error(f(166));
                    return Nt(e),
                    null
                }
                t = Q.current,
                va(e) ? ur(e) : (t = Rd(n, a, l),
                e.stateNode = t,
                Ie(e))
            }
            return Nt(e),
            null;
        case 5:
            if (Zn(e),
            n = e.type,
            t !== null && e.stateNode != null)
                t.memoizedProps !== a && Ie(e);
            else {
                if (!a) {
                    if (e.stateNode === null)
                        throw Error(f(166));
                    return Nt(e),
                    null
                }
                if (u = Q.current,
                va(e))
                    ur(e);
                else {
                    var c = ku(lt.current);
                    switch (u) {
                    case 1:
                        u = c.createElementNS("http://www.w3.org/2000/svg", n);
                        break;
                    case 2:
                        u = c.createElementNS("http://www.w3.org/1998/Math/MathML", n);
                        break;
                    default:
                        switch (n) {
                        case "svg":
                            u = c.createElementNS("http://www.w3.org/2000/svg", n);
                            break;
                        case "math":
                            u = c.createElementNS("http://www.w3.org/1998/Math/MathML", n);
                            break;
                        case "script":
                            u = c.createElement("div"),
                            u.innerHTML = "<script><\/script>",
                            u = u.removeChild(u.firstChild);
                            break;
                        case "select":
                            u = typeof a.is == "string" ? c.createElement("select", {
                                is: a.is
                            }) : c.createElement("select"),
                            a.multiple ? u.multiple = !0 : a.size && (u.size = a.size);
                            break;
                        default:
                            u = typeof a.is == "string" ? c.createElement(n, {
                                is: a.is
                            }) : c.createElement(n)
                        }
                    }
                    u[Qt] = e,
                    u[It] = a;
                    t: for (c = e.child; c !== null; ) {
                        if (c.tag === 5 || c.tag === 6)
                            u.appendChild(c.stateNode);
                        else if (c.tag !== 4 && c.tag !== 27 && c.child !== null) {
                            c.child.return = c,
                            c = c.child;
                            continue
                        }
                        if (c === e)
                            break t;
                        for (; c.sibling === null; ) {
                            if (c.return === null || c.return === e)
                                break t;
                            c = c.return
                        }
                        c.sibling.return = c.return,
                        c = c.sibling
                    }
                    e.stateNode = u;
                    t: switch (Jt(u, n, a),
                    n) {
                    case "button":
                    case "input":
                    case "select":
                    case "textarea":
                        a = !!a.autoFocus;
                        break t;
                    case "img":
                        a = !0;
                        break t;
                    default:
                        a = !1
                    }
                    a && Ie(e)
                }
            }
            return Nt(e),
            Kc(e, e.type, t === null ? null : t.memoizedProps, e.pendingProps, l),
            null;
        case 6:
            if (t && e.stateNode != null)
                t.memoizedProps !== a && Ie(e);
            else {
                if (typeof a != "string" && e.stateNode === null)
                    throw Error(f(166));
                if (t = lt.current,
                va(e)) {
                    if (t = e.stateNode,
                    l = e.memoizedProps,
                    a = null,
                    n = Zt,
                    n !== null)
                        switch (n.tag) {
                        case 27:
                        case 5:
                            a = n.memoizedProps
                        }
                    t[Qt] = e,
                    t = !!(t.nodeValue === l || a !== null && a.suppressHydrationWarning === !0 || jd(t.nodeValue, l)),
                    t || hl(e, !0)
                } else
                    t = ku(t).createTextNode(a),
                    t[Qt] = e,
                    e.stateNode = t
            }
            return Nt(e),
            null;
        case 31:
            if (l = e.memoizedState,
            t === null || t.memoizedState !== null) {
                if (a = va(e),
                l !== null) {
                    if (t === null) {
                        if (!a)
                            throw Error(f(318));
                        if (t = e.memoizedState,
                        t = t !== null ? t.dehydrated : null,
                        !t)
                            throw Error(f(557));
                        t[Qt] = e
                    } else
                        Ql(),
                        (e.flags & 128) === 0 && (e.memoizedState = null),
                        e.flags |= 4;
                    Nt(e),
                    t = !1
                } else
                    l = lc(),
                    t !== null && t.memoizedState !== null && (t.memoizedState.hydrationErrors = l),
                    t = !0;
                if (!t)
                    return e.flags & 256 ? (he(e),
                    e) : (he(e),
                    null);
                if ((e.flags & 128) !== 0)
                    throw Error(f(558))
            }
            return Nt(e),
            null;
        case 13:
            if (a = e.memoizedState,
            t === null || t.memoizedState !== null && t.memoizedState.dehydrated !== null) {
                if (n = va(e),
                a !== null && a.dehydrated !== null) {
                    if (t === null) {
                        if (!n)
                            throw Error(f(318));
                        if (n = e.memoizedState,
                        n = n !== null ? n.dehydrated : null,
                        !n)
                            throw Error(f(317));
                        n[Qt] = e
                    } else
                        Ql(),
                        (e.flags & 128) === 0 && (e.memoizedState = null),
                        e.flags |= 4;
                    Nt(e),
                    n = !1
                } else
                    n = lc(),
                    t !== null && t.memoizedState !== null && (t.memoizedState.hydrationErrors = n),
                    n = !0;
                if (!n)
                    return e.flags & 256 ? (he(e),
                    e) : (he(e),
                    null)
            }
            return he(e),
            (e.flags & 128) !== 0 ? (e.lanes = l,
            e) : (l = a !== null,
            t = t !== null && t.memoizedState !== null,
            l && (a = e.child,
            n = null,
            a.alternate !== null && a.alternate.memoizedState !== null && a.alternate.memoizedState.cachePool !== null && (n = a.alternate.memoizedState.cachePool.pool),
            u = null,
            a.memoizedState !== null && a.memoizedState.cachePool !== null && (u = a.memoizedState.cachePool.pool),
            u !== n && (a.flags |= 2048)),
            l !== t && l && (e.child.flags |= 8192),
            Cu(e, e.updateQueue),
            Nt(e),
            null);
        case 4:
            return Ot(),
            t === null && hs(e.stateNode.containerInfo),
            Nt(e),
            null;
        case 10:
            return ke(e.type),
            Nt(e),
            null;
        case 19:
            if (R(wt),
            a = e.memoizedState,
            a === null)
                return Nt(e),
                null;
            if (n = (e.flags & 128) !== 0,
            u = a.rendering,
            u === null)
                if (n)
                    pn(a, !1);
                else {
                    if (_t !== 0 || t !== null && (t.flags & 128) !== 0)
                        for (t = e.child; t !== null; ) {
                            if (u = bu(t),
                            u !== null) {
                                for (e.flags |= 128,
                                pn(a, !1),
                                t = u.updateQueue,
                                e.updateQueue = t,
                                Cu(e, t),
                                e.subtreeFlags = 0,
                                t = l,
                                l = e.child; l !== null; )
                                    tr(l, t),
                                    l = l.sibling;
                                return B(wt, wt.current & 1 | 2),
                                ct && Ke(e, a.treeForkCount),
                                e.child
                            }
                            t = t.sibling
                        }
                    a.tail !== null && se() > Bu && (e.flags |= 128,
                    n = !0,
                    pn(a, !1),
                    e.lanes = 4194304)
                }
            else {
                if (!n)
                    if (t = bu(u),
                    t !== null) {
                        if (e.flags |= 128,
                        n = !0,
                        t = t.updateQueue,
                        e.updateQueue = t,
                        Cu(e, t),
                        pn(a, !0),
                        a.tail === null && a.tailMode === "hidden" && !u.alternate && !ct)
                            return Nt(e),
                            null
                    } else
                        2 * se() - a.renderingStartTime > Bu && l !== 536870912 && (e.flags |= 128,
                        n = !0,
                        pn(a, !1),
                        e.lanes = 4194304);
                a.isBackwards ? (u.sibling = e.child,
                e.child = u) : (t = a.last,
                t !== null ? t.sibling = u : e.child = u,
                a.last = u)
            }
            return a.tail !== null ? (t = a.tail,
            a.rendering = t,
            a.tail = t.sibling,
            a.renderingStartTime = se(),
            t.sibling = null,
            l = wt.current,
            B(wt, n ? l & 1 | 2 : l & 1),
            ct && Ke(e, a.treeForkCount),
            t) : (Nt(e),
            null);
        case 22:
        case 23:
            return he(e),
            gc(),
            a = e.memoizedState !== null,
            t !== null ? t.memoizedState !== null !== a && (e.flags |= 8192) : a && (e.flags |= 8192),
            a ? (l & 536870912) !== 0 && (e.flags & 128) === 0 && (Nt(e),
            e.subtreeFlags & 6 && (e.flags |= 8192)) : Nt(e),
            l = e.updateQueue,
            l !== null && Cu(e, l.retryQueue),
            l = null,
            t !== null && t.memoizedState !== null && t.memoizedState.cachePool !== null && (l = t.memoizedState.cachePool.pool),
            a = null,
            e.memoizedState !== null && e.memoizedState.cachePool !== null && (a = e.memoizedState.cachePool.pool),
            a !== l && (e.flags |= 2048),
            t !== null && R(Kl),
            null;
        case 24:
            return l = null,
            t !== null && (l = t.memoizedState.cache),
            e.memoizedState.cache !== l && (e.flags |= 2048),
            ke(Ct),
            Nt(e),
            null;
        case 25:
            return null;
        case 30:
            return null
        }
        throw Error(f(156, e.tag))
    }
    function m0(t, e) {
        switch (tc(e),
        e.tag) {
        case 1:
            return t = e.flags,
            t & 65536 ? (e.flags = t & -65537 | 128,
            e) : null;
        case 3:
            return ke(Ct),
            Ot(),
            t = e.flags,
            (t & 65536) !== 0 && (t & 128) === 0 ? (e.flags = t & -65537 | 128,
            e) : null;
        case 26:
        case 27:
        case 5:
            return Zn(e),
            null;
        case 31:
            if (e.memoizedState !== null) {
                if (he(e),
                e.alternate === null)
                    throw Error(f(340));
                Ql()
            }
            return t = e.flags,
            t & 65536 ? (e.flags = t & -65537 | 128,
            e) : null;
        case 13:
            if (he(e),
            t = e.memoizedState,
            t !== null && t.dehydrated !== null) {
                if (e.alternate === null)
                    throw Error(f(340));
                Ql()
            }
            return t = e.flags,
            t & 65536 ? (e.flags = t & -65537 | 128,
            e) : null;
        case 19:
            return R(wt),
            null;
        case 4:
            return Ot(),
            null;
        case 10:
            return ke(e.type),
            null;
        case 22:
        case 23:
            return he(e),
            gc(),
            t !== null && R(Kl),
            t = e.flags,
            t & 65536 ? (e.flags = t & -65537 | 128,
            e) : null;
        case 24:
            return ke(Ct),
            null;
        case 25:
            return null;
        default:
            return null
        }
    }
    function _o(t, e) {
        switch (tc(e),
        e.tag) {
        case 3:
            ke(Ct),
            Ot();
            break;
        case 26:
        case 27:
        case 5:
            Zn(e);
            break;
        case 4:
            Ot();
            break;
        case 31:
            e.memoizedState !== null && he(e);
            break;
        case 13:
            he(e);
            break;
        case 19:
            R(wt);
            break;
        case 10:
            ke(e.type);
            break;
        case 22:
        case 23:
            he(e),
            gc(),
            t !== null && R(Kl);
            break;
        case 24:
            ke(Ct)
        }
    }
    function bn(t, e) {
        try {
            var l = e.updateQueue
              , a = l !== null ? l.lastEffect : null;
            if (a !== null) {
                var n = a.next;
                l = n;
                do {
                    if ((l.tag & t) === t) {
                        a = void 0;
                        var u = l.create
                          , c = l.inst;
                        a = u(),
                        c.destroy = a
                    }
                    l = l.next
                } while (l !== n)
            }
        } catch (r) {
            ht(e, e.return, r)
        }
    }
    function Sl(t, e, l) {
        try {
            var a = e.updateQueue
              , n = a !== null ? a.lastEffect : null;
            if (n !== null) {
                var u = n.next;
                a = u;
                do {
                    if ((a.tag & t) === t) {
                        var c = a.inst
                          , r = c.destroy;
                        if (r !== void 0) {
                            c.destroy = void 0,
                            n = e;
                            var h = l
                              , E = r;
                            try {
                                E()
                            } catch (O) {
                                ht(n, h, O)
                            }
                        }
                    }
                    a = a.next
                } while (a !== u)
            }
        } catch (O) {
            ht(e, e.return, O)
        }
    }
    function Mo(t) {
        var e = t.updateQueue;
        if (e !== null) {
            var l = t.stateNode;
            try {
                vr(e, l)
            } catch (a) {
                ht(t, t.return, a)
            }
        }
    }
    function Oo(t, e, l) {
        l.props = Fl(t.type, t.memoizedProps),
        l.state = t.memoizedState;
        try {
            l.componentWillUnmount()
        } catch (a) {
            ht(t, e, a)
        }
    }
    function Sn(t, e) {
        try {
            var l = t.ref;
            if (l !== null) {
                switch (t.tag) {
                case 26:
                case 27:
                case 5:
                    var a = t.stateNode;
                    break;
                case 30:
                    a = t.stateNode;
                    break;
                default:
                    a = t.stateNode
                }
                typeof l == "function" ? t.refCleanup = l(a) : l.current = a
            }
        } catch (n) {
            ht(t, e, n)
        }
    }
    function He(t, e) {
        var l = t.ref
          , a = t.refCleanup;
        if (l !== null)
            if (typeof a == "function")
                try {
                    a()
                } catch (n) {
                    ht(t, e, n)
                } finally {
                    t.refCleanup = null,
                    t = t.alternate,
                    t != null && (t.refCleanup = null)
                }
            else if (typeof l == "function")
                try {
                    l(null)
                } catch (n) {
                    ht(t, e, n)
                }
            else
                l.current = null
    }
    function wo(t) {
        var e = t.type
          , l = t.memoizedProps
          , a = t.stateNode;
        try {
            t: switch (e) {
            case "button":
            case "input":
            case "select":
            case "textarea":
                l.autoFocus && a.focus();
                break t;
            case "img":
                l.src ? a.src = l.src : l.srcSet && (a.srcset = l.srcSet)
            }
        } catch (n) {
            ht(t, t.return, n)
        }
    }
    function Jc(t, e, l) {
        try {
            var a = t.stateNode;
            U0(a, t.type, l, e),
            a[It] = e
        } catch (n) {
            ht(t, t.return, n)
        }
    }
    function Do(t) {
        return t.tag === 5 || t.tag === 3 || t.tag === 26 || t.tag === 27 && _l(t.type) || t.tag === 4
    }
    function kc(t) {
        t: for (; ; ) {
            for (; t.sibling === null; ) {
                if (t.return === null || Do(t.return))
                    return null;
                t = t.return
            }
            for (t.sibling.return = t.return,
            t = t.sibling; t.tag !== 5 && t.tag !== 6 && t.tag !== 18; ) {
                if (t.tag === 27 && _l(t.type) || t.flags & 2 || t.child === null || t.tag === 4)
                    continue t;
                t.child.return = t,
                t = t.child
            }
            if (!(t.flags & 2))
                return t.stateNode
        }
    }
    function $c(t, e, l) {
        var a = t.tag;
        if (a === 5 || a === 6)
            t = t.stateNode,
            e ? (l.nodeType === 9 ? l.body : l.nodeName === "HTML" ? l.ownerDocument.body : l).insertBefore(t, e) : (e = l.nodeType === 9 ? l.body : l.nodeName === "HTML" ? l.ownerDocument.body : l,
            e.appendChild(t),
            l = l._reactRootContainer,
            l != null || e.onclick !== null || (e.onclick = Qe));
        else if (a !== 4 && (a === 27 && _l(t.type) && (l = t.stateNode,
        e = null),
        t = t.child,
        t !== null))
            for ($c(t, e, l),
            t = t.sibling; t !== null; )
                $c(t, e, l),
                t = t.sibling
    }
    function Ru(t, e, l) {
        var a = t.tag;
        if (a === 5 || a === 6)
            t = t.stateNode,
            e ? l.insertBefore(t, e) : l.appendChild(t);
        else if (a !== 4 && (a === 27 && _l(t.type) && (l = t.stateNode),
        t = t.child,
        t !== null))
            for (Ru(t, e, l),
            t = t.sibling; t !== null; )
                Ru(t, e, l),
                t = t.sibling
    }
    function Co(t) {
        var e = t.stateNode
          , l = t.memoizedProps;
        try {
            for (var a = t.type, n = e.attributes; n.length; )
                e.removeAttributeNode(n[0]);
            Jt(e, a, l),
            e[Qt] = t,
            e[It] = l
        } catch (u) {
            ht(t, t.return, u)
        }
    }
    var Pe = !1
      , Ht = !1
      , Wc = !1
      , Ro = typeof WeakSet == "function" ? WeakSet : Set
      , Xt = null;
    function h0(t, e) {
        if (t = t.containerInfo,
        ys = ei,
        t = Vf(t),
        Qi(t)) {
            if ("selectionStart"in t)
                var l = {
                    start: t.selectionStart,
                    end: t.selectionEnd
                };
            else
                t: {
                    l = (l = t.ownerDocument) && l.defaultView || window;
                    var a = l.getSelection && l.getSelection();
                    if (a && a.rangeCount !== 0) {
                        l = a.anchorNode;
                        var n = a.anchorOffset
                          , u = a.focusNode;
                        a = a.focusOffset;
                        try {
                            l.nodeType,
                            u.nodeType
                        } catch {
                            l = null;
                            break t
                        }
                        var c = 0
                          , r = -1
                          , h = -1
                          , E = 0
                          , O = 0
                          , C = t
                          , z = null;
                        e: for (; ; ) {
                            for (var A; C !== l || n !== 0 && C.nodeType !== 3 || (r = c + n),
                            C !== u || a !== 0 && C.nodeType !== 3 || (h = c + a),
                            C.nodeType === 3 && (c += C.nodeValue.length),
                            (A = C.firstChild) !== null; )
                                z = C,
                                C = A;
                            for (; ; ) {
                                if (C === t)
                                    break e;
                                if (z === l && ++E === n && (r = c),
                                z === u && ++O === a && (h = c),
                                (A = C.nextSibling) !== null)
                                    break;
                                C = z,
                                z = C.parentNode
                            }
                            C = A
                        }
                        l = r === -1 || h === -1 ? null : {
                            start: r,
                            end: h
                        }
                    } else
                        l = null
                }
            l = l || {
                start: 0,
                end: 0
            }
        } else
            l = null;
        for (vs = {
            focusedElem: t,
            selectionRange: l
        },
        ei = !1,
        Xt = e; Xt !== null; )
            if (e = Xt,
            t = e.child,
            (e.subtreeFlags & 1028) !== 0 && t !== null)
                t.return = e,
                Xt = t;
            else
                for (; Xt !== null; ) {
                    switch (e = Xt,
                    u = e.alternate,
                    t = e.flags,
                    e.tag) {
                    case 0:
                        if ((t & 4) !== 0 && (t = e.updateQueue,
                        t = t !== null ? t.events : null,
                        t !== null))
                            for (l = 0; l < t.length; l++)
                                n = t[l],
                                n.ref.impl = n.nextImpl;
                        break;
                    case 11:
                    case 15:
                        break;
                    case 1:
                        if ((t & 1024) !== 0 && u !== null) {
                            t = void 0,
                            l = e,
                            n = u.memoizedProps,
                            u = u.memoizedState,
                            a = l.stateNode;
                            try {
                                var G = Fl(l.type, n);
                                t = a.getSnapshotBeforeUpdate(G, u),
                                a.__reactInternalSnapshotBeforeUpdate = t
                            } catch (k) {
                                ht(l, l.return, k)
                            }
                        }
                        break;
                    case 3:
                        if ((t & 1024) !== 0) {
                            if (t = e.stateNode.containerInfo,
                            l = t.nodeType,
                            l === 9)
                                Ss(t);
                            else if (l === 1)
                                switch (t.nodeName) {
                                case "HEAD":
                                case "HTML":
                                case "BODY":
                                    Ss(t);
                                    break;
                                default:
                                    t.textContent = ""
                                }
                        }
                        break;
                    case 5:
                    case 26:
                    case 27:
                    case 6:
                    case 4:
                    case 17:
                        break;
                    default:
                        if ((t & 1024) !== 0)
                            throw Error(f(163))
                    }
                    if (t = e.sibling,
                    t !== null) {
                        t.return = e.return,
                        Xt = t;
                        break
                    }
                    Xt = e.return
                }
    }
    function Uo(t, e, l) {
        var a = l.flags;
        switch (l.tag) {
        case 0:
        case 11:
        case 15:
            el(t, l),
            a & 4 && bn(5, l);
            break;
        case 1:
            if (el(t, l),
            a & 4)
                if (t = l.stateNode,
                e === null)
                    try {
                        t.componentDidMount()
                    } catch (c) {
                        ht(l, l.return, c)
                    }
                else {
                    var n = Fl(l.type, e.memoizedProps);
                    e = e.memoizedState;
                    try {
                        t.componentDidUpdate(n, e, t.__reactInternalSnapshotBeforeUpdate)
                    } catch (c) {
                        ht(l, l.return, c)
                    }
                }
            a & 64 && Mo(l),
            a & 512 && Sn(l, l.return);
            break;
        case 3:
            if (el(t, l),
            a & 64 && (t = l.updateQueue,
            t !== null)) {
                if (e = null,
                l.child !== null)
                    switch (l.child.tag) {
                    case 27:
                    case 5:
                        e = l.child.stateNode;
                        break;
                    case 1:
                        e = l.child.stateNode
                    }
                try {
                    vr(t, e)
                } catch (c) {
                    ht(l, l.return, c)
                }
            }
            break;
        case 27:
            e === null && a & 4 && Co(l);
        case 26:
        case 5:
            el(t, l),
            e === null && a & 4 && wo(l),
            a & 512 && Sn(l, l.return);
            break;
        case 12:
            el(t, l);
            break;
        case 31:
            el(t, l),
            a & 4 && Bo(t, l);
            break;
        case 13:
            el(t, l),
            a & 4 && Yo(t, l),
            a & 64 && (t = l.memoizedState,
            t !== null && (t = t.dehydrated,
            t !== null && (l = j0.bind(null, l),
            Q0(t, l))));
            break;
        case 22:
            if (a = l.memoizedState !== null || Pe,
            !a) {
                e = e !== null && e.memoizedState !== null || Ht,
                n = Pe;
                var u = Ht;
                Pe = a,
                (Ht = e) && !u ? ll(t, l, (l.subtreeFlags & 8772) !== 0) : el(t, l),
                Pe = n,
                Ht = u
            }
            break;
        case 30:
            break;
        default:
            el(t, l)
        }
    }
    function Ho(t) {
        var e = t.alternate;
        e !== null && (t.alternate = null,
        Ho(e)),
        t.child = null,
        t.deletions = null,
        t.sibling = null,
        t.tag === 5 && (e = t.stateNode,
        e !== null && Ti(e)),
        t.stateNode = null,
        t.return = null,
        t.dependencies = null,
        t.memoizedProps = null,
        t.memoizedState = null,
        t.pendingProps = null,
        t.stateNode = null,
        t.updateQueue = null
    }
    var jt = null
      , te = !1;
    function tl(t, e, l) {
        for (l = l.child; l !== null; )
            qo(t, e, l),
            l = l.sibling
    }
    function qo(t, e, l) {
        if (fe && typeof fe.onCommitFiberUnmount == "function")
            try {
                fe.onCommitFiberUnmount(Za, l)
            } catch {}
        switch (l.tag) {
        case 26:
            Ht || He(l, e),
            tl(t, e, l),
            l.memoizedState ? l.memoizedState.count-- : l.stateNode && (l = l.stateNode,
            l.parentNode.removeChild(l));
            break;
        case 27:
            Ht || He(l, e);
            var a = jt
              , n = te;
            _l(l.type) && (jt = l.stateNode,
            te = !1),
            tl(t, e, l),
            On(l.stateNode),
            jt = a,
            te = n;
            break;
        case 5:
            Ht || He(l, e);
        case 6:
            if (a = jt,
            n = te,
            jt = null,
            tl(t, e, l),
            jt = a,
            te = n,
            jt !== null)
                if (te)
                    try {
                        (jt.nodeType === 9 ? jt.body : jt.nodeName === "HTML" ? jt.ownerDocument.body : jt).removeChild(l.stateNode)
                    } catch (u) {
                        ht(l, e, u)
                    }
                else
                    try {
                        jt.removeChild(l.stateNode)
                    } catch (u) {
                        ht(l, e, u)
                    }
            break;
        case 18:
            jt !== null && (te ? (t = jt,
            Md(t.nodeType === 9 ? t.body : t.nodeName === "HTML" ? t.ownerDocument.body : t, l.stateNode),
            Ya(t)) : Md(jt, l.stateNode));
            break;
        case 4:
            a = jt,
            n = te,
            jt = l.stateNode.containerInfo,
            te = !0,
            tl(t, e, l),
            jt = a,
            te = n;
            break;
        case 0:
        case 11:
        case 14:
        case 15:
            Sl(2, l, e),
            Ht || Sl(4, l, e),
            tl(t, e, l);
            break;
        case 1:
            Ht || (He(l, e),
            a = l.stateNode,
            typeof a.componentWillUnmount == "function" && Oo(l, e, a)),
            tl(t, e, l);
            break;
        case 21:
            tl(t, e, l);
            break;
        case 22:
            Ht = (a = Ht) || l.memoizedState !== null,
            tl(t, e, l),
            Ht = a;
            break;
        default:
            tl(t, e, l)
        }
    }
    function Bo(t, e) {
        if (e.memoizedState === null && (t = e.alternate,
        t !== null && (t = t.memoizedState,
        t !== null))) {
            t = t.dehydrated;
            try {
                Ya(t)
            } catch (l) {
                ht(e, e.return, l)
            }
        }
    }
    function Yo(t, e) {
        if (e.memoizedState === null && (t = e.alternate,
        t !== null && (t = t.memoizedState,
        t !== null && (t = t.dehydrated,
        t !== null))))
            try {
                Ya(t)
            } catch (l) {
                ht(e, e.return, l)
            }
    }
    function g0(t) {
        switch (t.tag) {
        case 31:
        case 13:
        case 19:
            var e = t.stateNode;
            return e === null && (e = t.stateNode = new Ro),
            e;
        case 22:
            return t = t.stateNode,
            e = t._retryCache,
            e === null && (e = t._retryCache = new Ro),
            e;
        default:
            throw Error(f(435, t.tag))
        }
    }
    function Uu(t, e) {
        var l = g0(t);
        e.forEach(function(a) {
            if (!l.has(a)) {
                l.add(a);
                var n = E0.bind(null, t, a);
                a.then(n, n)
            }
        })
    }
    function ee(t, e) {
        var l = e.deletions;
        if (l !== null)
            for (var a = 0; a < l.length; a++) {
                var n = l[a]
                  , u = t
                  , c = e
                  , r = c;
                t: for (; r !== null; ) {
                    switch (r.tag) {
                    case 27:
                        if (_l(r.type)) {
                            jt = r.stateNode,
                            te = !1;
                            break t
                        }
                        break;
                    case 5:
                        jt = r.stateNode,
                        te = !1;
                        break t;
                    case 3:
                    case 4:
                        jt = r.stateNode.containerInfo,
                        te = !0;
                        break t
                    }
                    r = r.return
                }
                if (jt === null)
                    throw Error(f(160));
                qo(u, c, n),
                jt = null,
                te = !1,
                u = n.alternate,
                u !== null && (u.return = null),
                n.return = null
            }
        if (e.subtreeFlags & 13886)
            for (e = e.child; e !== null; )
                Lo(e, t),
                e = e.sibling
    }
    var we = null;
    function Lo(t, e) {
        var l = t.alternate
          , a = t.flags;
        switch (t.tag) {
        case 0:
        case 11:
        case 14:
        case 15:
            ee(e, t),
            le(t),
            a & 4 && (Sl(3, t, t.return),
            bn(3, t),
            Sl(5, t, t.return));
            break;
        case 1:
            ee(e, t),
            le(t),
            a & 512 && (Ht || l === null || He(l, l.return)),
            a & 64 && Pe && (t = t.updateQueue,
            t !== null && (a = t.callbacks,
            a !== null && (l = t.shared.hiddenCallbacks,
            t.shared.hiddenCallbacks = l === null ? a : l.concat(a))));
            break;
        case 26:
            var n = we;
            if (ee(e, t),
            le(t),
            a & 512 && (Ht || l === null || He(l, l.return)),
            a & 4) {
                var u = l !== null ? l.memoizedState : null;
                if (a = t.memoizedState,
                l === null)
                    if (a === null)
                        if (t.stateNode === null) {
                            t: {
                                a = t.type,
                                l = t.memoizedProps,
                                n = n.ownerDocument || n;
                                e: switch (a) {
                                case "title":
                                    u = n.getElementsByTagName("title")[0],
                                    (!u || u[Ja] || u[Qt] || u.namespaceURI === "http://www.w3.org/2000/svg" || u.hasAttribute("itemprop")) && (u = n.createElement(a),
                                    n.head.insertBefore(u, n.querySelector("head > title"))),
                                    Jt(u, a, l),
                                    u[Qt] = t,
                                    Gt(u),
                                    a = u;
                                    break t;
                                case "link":
                                    var c = Ld("link", "href", n).get(a + (l.href || ""));
                                    if (c) {
                                        for (var r = 0; r < c.length; r++)
                                            if (u = c[r],
                                            u.getAttribute("href") === (l.href == null || l.href === "" ? null : l.href) && u.getAttribute("rel") === (l.rel == null ? null : l.rel) && u.getAttribute("title") === (l.title == null ? null : l.title) && u.getAttribute("crossorigin") === (l.crossOrigin == null ? null : l.crossOrigin)) {
                                                c.splice(r, 1);
                                                break e
                                            }
                                    }
                                    u = n.createElement(a),
                                    Jt(u, a, l),
                                    n.head.appendChild(u);
                                    break;
                                case "meta":
                                    if (c = Ld("meta", "content", n).get(a + (l.content || ""))) {
                                        for (r = 0; r < c.length; r++)
                                            if (u = c[r],
                                            u.getAttribute("content") === (l.content == null ? null : "" + l.content) && u.getAttribute("name") === (l.name == null ? null : l.name) && u.getAttribute("property") === (l.property == null ? null : l.property) && u.getAttribute("http-equiv") === (l.httpEquiv == null ? null : l.httpEquiv) && u.getAttribute("charset") === (l.charSet == null ? null : l.charSet)) {
                                                c.splice(r, 1);
                                                break e
                                            }
                                    }
                                    u = n.createElement(a),
                                    Jt(u, a, l),
                                    n.head.appendChild(u);
                                    break;
                                default:
                                    throw Error(f(468, a))
                                }
                                u[Qt] = t,
                                Gt(u),
                                a = u
                            }
                            t.stateNode = a
                        } else
                            Gd(n, t.type, t.stateNode);
                    else
                        t.stateNode = Yd(n, a, t.memoizedProps);
                else
                    u !== a ? (u === null ? l.stateNode !== null && (l = l.stateNode,
                    l.parentNode.removeChild(l)) : u.count--,
                    a === null ? Gd(n, t.type, t.stateNode) : Yd(n, a, t.memoizedProps)) : a === null && t.stateNode !== null && Jc(t, t.memoizedProps, l.memoizedProps)
            }
            break;
        case 27:
            ee(e, t),
            le(t),
            a & 512 && (Ht || l === null || He(l, l.return)),
            l !== null && a & 4 && Jc(t, t.memoizedProps, l.memoizedProps);
            break;
        case 5:
            if (ee(e, t),
            le(t),
            a & 512 && (Ht || l === null || He(l, l.return)),
            t.flags & 32) {
                n = t.stateNode;
                try {
                    sa(n, "")
                } catch (G) {
                    ht(t, t.return, G)
                }
            }
            a & 4 && t.stateNode != null && (n = t.memoizedProps,
            Jc(t, n, l !== null ? l.memoizedProps : n)),
            a & 1024 && (Wc = !0);
            break;
        case 6:
            if (ee(e, t),
            le(t),
            a & 4) {
                if (t.stateNode === null)
                    throw Error(f(162));
                a = t.memoizedProps,
                l = t.stateNode;
                try {
                    l.nodeValue = a
                } catch (G) {
                    ht(t, t.return, G)
                }
            }
            break;
        case 3:
            if (Fu = null,
            n = we,
            we = $u(e.containerInfo),
            ee(e, t),
            we = n,
            le(t),
            a & 4 && l !== null && l.memoizedState.isDehydrated)
                try {
                    Ya(e.containerInfo)
                } catch (G) {
                    ht(t, t.return, G)
                }
            Wc && (Wc = !1,
            Go(t));
            break;
        case 4:
            a = we,
            we = $u(t.stateNode.containerInfo),
            ee(e, t),
            le(t),
            we = a;
            break;
        case 12:
            ee(e, t),
            le(t);
            break;
        case 31:
            ee(e, t),
            le(t),
            a & 4 && (a = t.updateQueue,
            a !== null && (t.updateQueue = null,
            Uu(t, a)));
            break;
        case 13:
            ee(e, t),
            le(t),
            t.child.flags & 8192 && t.memoizedState !== null != (l !== null && l.memoizedState !== null) && (qu = se()),
            a & 4 && (a = t.updateQueue,
            a !== null && (t.updateQueue = null,
            Uu(t, a)));
            break;
        case 22:
            n = t.memoizedState !== null;
            var h = l !== null && l.memoizedState !== null
              , E = Pe
              , O = Ht;
            if (Pe = E || n,
            Ht = O || h,
            ee(e, t),
            Ht = O,
            Pe = E,
            le(t),
            a & 8192)
                t: for (e = t.stateNode,
                e._visibility = n ? e._visibility & -2 : e._visibility | 1,
                n && (l === null || h || Pe || Ht || Il(t)),
                l = null,
                e = t; ; ) {
                    if (e.tag === 5 || e.tag === 26) {
                        if (l === null) {
                            h = l = e;
                            try {
                                if (u = h.stateNode,
                                n)
                                    c = u.style,
                                    typeof c.setProperty == "function" ? c.setProperty("display", "none", "important") : c.display = "none";
                                else {
                                    r = h.stateNode;
                                    var C = h.memoizedProps.style
                                      , z = C != null && C.hasOwnProperty("display") ? C.display : null;
                                    r.style.display = z == null || typeof z == "boolean" ? "" : ("" + z).trim()
                                }
                            } catch (G) {
                                ht(h, h.return, G)
                            }
                        }
                    } else if (e.tag === 6) {
                        if (l === null) {
                            h = e;
                            try {
                                h.stateNode.nodeValue = n ? "" : h.memoizedProps
                            } catch (G) {
                                ht(h, h.return, G)
                            }
                        }
                    } else if (e.tag === 18) {
                        if (l === null) {
                            h = e;
                            try {
                                var A = h.stateNode;
                                n ? Od(A, !0) : Od(h.stateNode, !1)
                            } catch (G) {
                                ht(h, h.return, G)
                            }
                        }
                    } else if ((e.tag !== 22 && e.tag !== 23 || e.memoizedState === null || e === t) && e.child !== null) {
                        e.child.return = e,
                        e = e.child;
                        continue
                    }
                    if (e === t)
                        break t;
                    for (; e.sibling === null; ) {
                        if (e.return === null || e.return === t)
                            break t;
                        l === e && (l = null),
                        e = e.return
                    }
                    l === e && (l = null),
                    e.sibling.return = e.return,
                    e = e.sibling
                }
            a & 4 && (a = t.updateQueue,
            a !== null && (l = a.retryQueue,
            l !== null && (a.retryQueue = null,
            Uu(t, l))));
            break;
        case 19:
            ee(e, t),
            le(t),
            a & 4 && (a = t.updateQueue,
            a !== null && (t.updateQueue = null,
            Uu(t, a)));
            break;
        case 30:
            break;
        case 21:
            break;
        default:
            ee(e, t),
            le(t)
        }
    }
    function le(t) {
        var e = t.flags;
        if (e & 2) {
            try {
                for (var l, a = t.return; a !== null; ) {
                    if (Do(a)) {
                        l = a;
                        break
                    }
                    a = a.return
                }
                if (l == null)
                    throw Error(f(160));
                switch (l.tag) {
                case 27:
                    var n = l.stateNode
                      , u = kc(t);
                    Ru(t, u, n);
                    break;
                case 5:
                    var c = l.stateNode;
                    l.flags & 32 && (sa(c, ""),
                    l.flags &= -33);
                    var r = kc(t);
                    Ru(t, r, c);
                    break;
                case 3:
                case 4:
                    var h = l.stateNode.containerInfo
                      , E = kc(t);
                    $c(t, E, h);
                    break;
                default:
                    throw Error(f(161))
                }
            } catch (O) {
                ht(t, t.return, O)
            }
            t.flags &= -3
        }
        e & 4096 && (t.flags &= -4097)
    }
    function Go(t) {
        if (t.subtreeFlags & 1024)
            for (t = t.child; t !== null; ) {
                var e = t;
                Go(e),
                e.tag === 5 && e.flags & 1024 && e.stateNode.reset(),
                t = t.sibling
            }
    }
    function el(t, e) {
        if (e.subtreeFlags & 8772)
            for (e = e.child; e !== null; )
                Uo(t, e.alternate, e),
                e = e.sibling
    }
    function Il(t) {
        for (t = t.child; t !== null; ) {
            var e = t;
            switch (e.tag) {
            case 0:
            case 11:
            case 14:
            case 15:
                Sl(4, e, e.return),
                Il(e);
                break;
            case 1:
                He(e, e.return);
                var l = e.stateNode;
                typeof l.componentWillUnmount == "function" && Oo(e, e.return, l),
                Il(e);
                break;
            case 27:
                On(e.stateNode);
            case 26:
            case 5:
                He(e, e.return),
                Il(e);
                break;
            case 22:
                e.memoizedState === null && Il(e);
                break;
            case 30:
                Il(e);
                break;
            default:
                Il(e)
            }
            t = t.sibling
        }
    }
    function ll(t, e, l) {
        for (l = l && (e.subtreeFlags & 8772) !== 0,
        e = e.child; e !== null; ) {
            var a = e.alternate
              , n = t
              , u = e
              , c = u.flags;
            switch (u.tag) {
            case 0:
            case 11:
            case 15:
                ll(n, u, l),
                bn(4, u);
                break;
            case 1:
                if (ll(n, u, l),
                a = u,
                n = a.stateNode,
                typeof n.componentDidMount == "function")
                    try {
                        n.componentDidMount()
                    } catch (E) {
                        ht(a, a.return, E)
                    }
                if (a = u,
                n = a.updateQueue,
                n !== null) {
                    var r = a.stateNode;
                    try {
                        var h = n.shared.hiddenCallbacks;
                        if (h !== null)
                            for (n.shared.hiddenCallbacks = null,
                            n = 0; n < h.length; n++)
                                yr(h[n], r)
                    } catch (E) {
                        ht(a, a.return, E)
                    }
                }
                l && c & 64 && Mo(u),
                Sn(u, u.return);
                break;
            case 27:
                Co(u);
            case 26:
            case 5:
                ll(n, u, l),
                l && a === null && c & 4 && wo(u),
                Sn(u, u.return);
                break;
            case 12:
                ll(n, u, l);
                break;
            case 31:
                ll(n, u, l),
                l && c & 4 && Bo(n, u);
                break;
            case 13:
                ll(n, u, l),
                l && c & 4 && Yo(n, u);
                break;
            case 22:
                u.memoizedState === null && ll(n, u, l),
                Sn(u, u.return);
                break;
            case 30:
                break;
            default:
                ll(n, u, l)
            }
            e = e.sibling
        }
    }
    function Fc(t, e) {
        var l = null;
        t !== null && t.memoizedState !== null && t.memoizedState.cachePool !== null && (l = t.memoizedState.cachePool.pool),
        t = null,
        e.memoizedState !== null && e.memoizedState.cachePool !== null && (t = e.memoizedState.cachePool.pool),
        t !== l && (t != null && t.refCount++,
        l != null && cn(l))
    }
    function Ic(t, e) {
        t = null,
        e.alternate !== null && (t = e.alternate.memoizedState.cache),
        e = e.memoizedState.cache,
        e !== t && (e.refCount++,
        t != null && cn(t))
    }
    function De(t, e, l, a) {
        if (e.subtreeFlags & 10256)
            for (e = e.child; e !== null; )
                Xo(t, e, l, a),
                e = e.sibling
    }
    function Xo(t, e, l, a) {
        var n = e.flags;
        switch (e.tag) {
        case 0:
        case 11:
        case 15:
            De(t, e, l, a),
            n & 2048 && bn(9, e);
            break;
        case 1:
            De(t, e, l, a);
            break;
        case 3:
            De(t, e, l, a),
            n & 2048 && (t = null,
            e.alternate !== null && (t = e.alternate.memoizedState.cache),
            e = e.memoizedState.cache,
            e !== t && (e.refCount++,
            t != null && cn(t)));
            break;
        case 12:
            if (n & 2048) {
                De(t, e, l, a),
                t = e.stateNode;
                try {
                    var u = e.memoizedProps
                      , c = u.id
                      , r = u.onPostCommit;
                    typeof r == "function" && r(c, e.alternate === null ? "mount" : "update", t.passiveEffectDuration, -0)
                } catch (h) {
                    ht(e, e.return, h)
                }
            } else
                De(t, e, l, a);
            break;
        case 31:
            De(t, e, l, a);
            break;
        case 13:
            De(t, e, l, a);
            break;
        case 23:
            break;
        case 22:
            u = e.stateNode,
            c = e.alternate,
            e.memoizedState !== null ? u._visibility & 2 ? De(t, e, l, a) : Nn(t, e) : u._visibility & 2 ? De(t, e, l, a) : (u._visibility |= 2,
            _a(t, e, l, a, (e.subtreeFlags & 10256) !== 0 || !1)),
            n & 2048 && Fc(c, e);
            break;
        case 24:
            De(t, e, l, a),
            n & 2048 && Ic(e.alternate, e);
            break;
        default:
            De(t, e, l, a)
        }
    }
    function _a(t, e, l, a, n) {
        for (n = n && ((e.subtreeFlags & 10256) !== 0 || !1),
        e = e.child; e !== null; ) {
            var u = t
              , c = e
              , r = l
              , h = a
              , E = c.flags;
            switch (c.tag) {
            case 0:
            case 11:
            case 15:
                _a(u, c, r, h, n),
                bn(8, c);
                break;
            case 23:
                break;
            case 22:
                var O = c.stateNode;
                c.memoizedState !== null ? O._visibility & 2 ? _a(u, c, r, h, n) : Nn(u, c) : (O._visibility |= 2,
                _a(u, c, r, h, n)),
                n && E & 2048 && Fc(c.alternate, c);
                break;
            case 24:
                _a(u, c, r, h, n),
                n && E & 2048 && Ic(c.alternate, c);
                break;
            default:
                _a(u, c, r, h, n)
            }
            e = e.sibling
        }
    }
    function Nn(t, e) {
        if (e.subtreeFlags & 10256)
            for (e = e.child; e !== null; ) {
                var l = t
                  , a = e
                  , n = a.flags;
                switch (a.tag) {
                case 22:
                    Nn(l, a),
                    n & 2048 && Fc(a.alternate, a);
                    break;
                case 24:
                    Nn(l, a),
                    n & 2048 && Ic(a.alternate, a);
                    break;
                default:
                    Nn(l, a)
                }
                e = e.sibling
            }
    }
    var jn = 8192;
    function Ma(t, e, l) {
        if (t.subtreeFlags & jn)
            for (t = t.child; t !== null; )
                Qo(t, e, l),
                t = t.sibling
    }
    function Qo(t, e, l) {
        switch (t.tag) {
        case 26:
            Ma(t, e, l),
            t.flags & jn && t.memoizedState !== null && eg(l, we, t.memoizedState, t.memoizedProps);
            break;
        case 5:
            Ma(t, e, l);
            break;
        case 3:
        case 4:
            var a = we;
            we = $u(t.stateNode.containerInfo),
            Ma(t, e, l),
            we = a;
            break;
        case 22:
            t.memoizedState === null && (a = t.alternate,
            a !== null && a.memoizedState !== null ? (a = jn,
            jn = 16777216,
            Ma(t, e, l),
            jn = a) : Ma(t, e, l));
            break;
        default:
            Ma(t, e, l)
        }
    }
    function Zo(t) {
        var e = t.alternate;
        if (e !== null && (t = e.child,
        t !== null)) {
            e.child = null;
            do
                e = t.sibling,
                t.sibling = null,
                t = e;
            while (t !== null)
        }
    }
    function En(t) {
        var e = t.deletions;
        if ((t.flags & 16) !== 0) {
            if (e !== null)
                for (var l = 0; l < e.length; l++) {
                    var a = e[l];
                    Xt = a,
                    Ko(a, t)
                }
            Zo(t)
        }
        if (t.subtreeFlags & 10256)
            for (t = t.child; t !== null; )
                Vo(t),
                t = t.sibling
    }
    function Vo(t) {
        switch (t.tag) {
        case 0:
        case 11:
        case 15:
            En(t),
            t.flags & 2048 && Sl(9, t, t.return);
            break;
        case 3:
            En(t);
            break;
        case 12:
            En(t);
            break;
        case 22:
            var e = t.stateNode;
            t.memoizedState !== null && e._visibility & 2 && (t.return === null || t.return.tag !== 13) ? (e._visibility &= -3,
            Hu(t)) : En(t);
            break;
        default:
            En(t)
        }
    }
    function Hu(t) {
        var e = t.deletions;
        if ((t.flags & 16) !== 0) {
            if (e !== null)
                for (var l = 0; l < e.length; l++) {
                    var a = e[l];
                    Xt = a,
                    Ko(a, t)
                }
            Zo(t)
        }
        for (t = t.child; t !== null; ) {
            switch (e = t,
            e.tag) {
            case 0:
            case 11:
            case 15:
                Sl(8, e, e.return),
                Hu(e);
                break;
            case 22:
                l = e.stateNode,
                l._visibility & 2 && (l._visibility &= -3,
                Hu(e));
                break;
            default:
                Hu(e)
            }
            t = t.sibling
        }
    }
    function Ko(t, e) {
        for (; Xt !== null; ) {
            var l = Xt;
            switch (l.tag) {
            case 0:
            case 11:
            case 15:
                Sl(8, l, e);
                break;
            case 23:
            case 22:
                if (l.memoizedState !== null && l.memoizedState.cachePool !== null) {
                    var a = l.memoizedState.cachePool.pool;
                    a != null && a.refCount++
                }
                break;
            case 24:
                cn(l.memoizedState.cache)
            }
            if (a = l.child,
            a !== null)
                a.return = l,
                Xt = a;
            else
                t: for (l = t; Xt !== null; ) {
                    a = Xt;
                    var n = a.sibling
                      , u = a.return;
                    if (Ho(a),
                    a === l) {
                        Xt = null;
                        break t
                    }
                    if (n !== null) {
                        n.return = u,
                        Xt = n;
                        break t
                    }
                    Xt = u
                }
        }
    }
    var x0 = {
        getCacheForType: function(t) {
            var e = Vt(Ct)
              , l = e.data.get(t);
            return l === void 0 && (l = t(),
            e.data.set(t, l)),
            l
        },
        cacheSignal: function() {
            return Vt(Ct).controller.signal
        }
    }
      , y0 = typeof WeakMap == "function" ? WeakMap : Map
      , rt = 0
      , bt = null
      , at = null
      , ut = 0
      , mt = 0
      , ge = null
      , Nl = !1
      , Oa = !1
      , Pc = !1
      , al = 0
      , _t = 0
      , jl = 0
      , Pl = 0
      , ts = 0
      , xe = 0
      , wa = 0
      , zn = null
      , ae = null
      , es = !1
      , qu = 0
      , Jo = 0
      , Bu = 1 / 0
      , Yu = null
      , El = null
      , Yt = 0
      , zl = null
      , Da = null
      , nl = 0
      , ls = 0
      , as = null
      , ko = null
      , Tn = 0
      , ns = null;
    function ye() {
        return (rt & 2) !== 0 && ut !== 0 ? ut & -ut : w.T !== null ? rs() : ff()
    }
    function $o() {
        if (xe === 0)
            if ((ut & 536870912) === 0 || ct) {
                var t = Jn;
                Jn <<= 1,
                (Jn & 3932160) === 0 && (Jn = 262144),
                xe = t
            } else
                xe = 536870912;
        return t = me.current,
        t !== null && (t.flags |= 32),
        xe
    }
    function ne(t, e, l) {
        (t === bt && (mt === 2 || mt === 9) || t.cancelPendingCommit !== null) && (Ca(t, 0),
        Tl(t, ut, xe, !1)),
        Ka(t, l),
        ((rt & 2) === 0 || t !== bt) && (t === bt && ((rt & 2) === 0 && (Pl |= l),
        _t === 4 && Tl(t, ut, xe, !1)),
        qe(t))
    }
    function Wo(t, e, l) {
        if ((rt & 6) !== 0)
            throw Error(f(327));
        var a = !l && (e & 127) === 0 && (e & t.expiredLanes) === 0 || Va(t, e)
          , n = a ? b0(t, e) : is(t, e, !0)
          , u = a;
        do {
            if (n === 0) {
                Oa && !a && Tl(t, e, 0, !1);
                break
            } else {
                if (l = t.current.alternate,
                u && !v0(l)) {
                    n = is(t, e, !1),
                    u = !1;
                    continue
                }
                if (n === 2) {
                    if (u = e,
                    t.errorRecoveryDisabledLanes & u)
                        var c = 0;
                    else
                        c = t.pendingLanes & -536870913,
                        c = c !== 0 ? c : c & 536870912 ? 536870912 : 0;
                    if (c !== 0) {
                        e = c;
                        t: {
                            var r = t;
                            n = zn;
                            var h = r.current.memoizedState.isDehydrated;
                            if (h && (Ca(r, c).flags |= 256),
                            c = is(r, c, !1),
                            c !== 2) {
                                if (Pc && !h) {
                                    r.errorRecoveryDisabledLanes |= u,
                                    Pl |= u,
                                    n = 4;
                                    break t
                                }
                                u = ae,
                                ae = n,
                                u !== null && (ae === null ? ae = u : ae.push.apply(ae, u))
                            }
                            n = c
                        }
                        if (u = !1,
                        n !== 2)
                            continue
                    }
                }
                if (n === 1) {
                    Ca(t, 0),
                    Tl(t, e, 0, !0);
                    break
                }
                t: {
                    switch (a = t,
                    u = n,
                    u) {
                    case 0:
                    case 1:
                        throw Error(f(345));
                    case 4:
                        if ((e & 4194048) !== e)
                            break;
                    case 6:
                        Tl(a, e, xe, !Nl);
                        break t;
                    case 2:
                        ae = null;
                        break;
                    case 3:
                    case 5:
                        break;
                    default:
                        throw Error(f(329))
                    }
                    if ((e & 62914560) === e && (n = qu + 300 - se(),
                    10 < n)) {
                        if (Tl(a, e, xe, !Nl),
                        $n(a, 0, !0) !== 0)
                            break t;
                        nl = e,
                        a.timeoutHandle = Ad(Fo.bind(null, a, l, ae, Yu, es, e, xe, Pl, wa, Nl, u, "Throttled", -0, 0), n);
                        break t
                    }
                    Fo(a, l, ae, Yu, es, e, xe, Pl, wa, Nl, u, null, -0, 0)
                }
            }
            break
        } while (!0);
        qe(t)
    }
    function Fo(t, e, l, a, n, u, c, r, h, E, O, C, z, A) {
        if (t.timeoutHandle = -1,
        C = e.subtreeFlags,
        C & 8192 || (C & 16785408) === 16785408) {
            C = {
                stylesheets: null,
                count: 0,
                imgCount: 0,
                imgBytes: 0,
                suspenseyImages: [],
                waitingForImages: !0,
                waitingForViewTransition: !1,
                unsuspend: Qe
            },
            Qo(e, u, C);
            var G = (u & 62914560) === u ? qu - se() : (u & 4194048) === u ? Jo - se() : 0;
            if (G = lg(C, G),
            G !== null) {
                nl = u,
                t.cancelPendingCommit = G(ud.bind(null, t, e, u, l, a, n, c, r, h, O, C, null, z, A)),
                Tl(t, u, c, !E);
                return
            }
        }
        ud(t, e, u, l, a, n, c, r, h)
    }
    function v0(t) {
        for (var e = t; ; ) {
            var l = e.tag;
            if ((l === 0 || l === 11 || l === 15) && e.flags & 16384 && (l = e.updateQueue,
            l !== null && (l = l.stores,
            l !== null)))
                for (var a = 0; a < l.length; a++) {
                    var n = l[a]
                      , u = n.getSnapshot;
                    n = n.value;
                    try {
                        if (!oe(u(), n))
                            return !1
                    } catch {
                        return !1
                    }
                }
            if (l = e.child,
            e.subtreeFlags & 16384 && l !== null)
                l.return = e,
                e = l;
            else {
                if (e === t)
                    break;
                for (; e.sibling === null; ) {
                    if (e.return === null || e.return === t)
                        return !0;
                    e = e.return
                }
                e.sibling.return = e.return,
                e = e.sibling
            }
        }
        return !0
    }
    function Tl(t, e, l, a) {
        e &= ~ts,
        e &= ~Pl,
        t.suspendedLanes |= e,
        t.pingedLanes &= ~e,
        a && (t.warmLanes |= e),
        a = t.expirationTimes;
        for (var n = e; 0 < n; ) {
            var u = 31 - re(n)
              , c = 1 << u;
            a[u] = -1,
            n &= ~c
        }
        l !== 0 && uf(t, l, e)
    }
    function Lu() {
        return (rt & 6) === 0 ? (An(0),
        !1) : !0
    }
    function us() {
        if (at !== null) {
            if (mt === 0)
                var t = at.return;
            else
                t = at,
                Je = Zl = null,
                Sc(t),
                ja = null,
                fn = 0,
                t = at;
            for (; t !== null; )
                _o(t.alternate, t),
                t = t.return;
            at = null
        }
    }
    function Ca(t, e) {
        var l = t.timeoutHandle;
        l !== -1 && (t.timeoutHandle = -1,
        B0(l)),
        l = t.cancelPendingCommit,
        l !== null && (t.cancelPendingCommit = null,
        l()),
        nl = 0,
        us(),
        bt = t,
        at = l = Ve(t.current, null),
        ut = e,
        mt = 0,
        ge = null,
        Nl = !1,
        Oa = Va(t, e),
        Pc = !1,
        wa = xe = ts = Pl = jl = _t = 0,
        ae = zn = null,
        es = !1,
        (e & 8) !== 0 && (e |= e & 32);
        var a = t.entangledLanes;
        if (a !== 0)
            for (t = t.entanglements,
            a &= e; 0 < a; ) {
                var n = 31 - re(a)
                  , u = 1 << n;
                e |= t[n],
                a &= ~u
            }
        return al = e,
        cu(),
        l
    }
    function Io(t, e) {
        I = null,
        w.H = yn,
        e === Na || e === gu ? (e = mr(),
        mt = 3) : e === fc ? (e = mr(),
        mt = 4) : mt = e === qc ? 8 : e !== null && typeof e == "object" && typeof e.then == "function" ? 6 : 1,
        ge = e,
        at === null && (_t = 1,
        Mu(t, Se(e, t.current)))
    }
    function Po() {
        var t = me.current;
        return t === null ? !0 : (ut & 4194048) === ut ? ze === null : (ut & 62914560) === ut || (ut & 536870912) !== 0 ? t === ze : !1
    }
    function td() {
        var t = w.H;
        return w.H = yn,
        t === null ? yn : t
    }
    function ed() {
        var t = w.A;
        return w.A = x0,
        t
    }
    function Gu() {
        _t = 4,
        Nl || (ut & 4194048) !== ut && me.current !== null || (Oa = !0),
        (jl & 134217727) === 0 && (Pl & 134217727) === 0 || bt === null || Tl(bt, ut, xe, !1)
    }
    function is(t, e, l) {
        var a = rt;
        rt |= 2;
        var n = td()
          , u = ed();
        (bt !== t || ut !== e) && (Yu = null,
        Ca(t, e)),
        e = !1;
        var c = _t;
        t: do
            try {
                if (mt !== 0 && at !== null) {
                    var r = at
                      , h = ge;
                    switch (mt) {
                    case 8:
                        us(),
                        c = 6;
                        break t;
                    case 3:
                    case 2:
                    case 9:
                    case 6:
                        me.current === null && (e = !0);
                        var E = mt;
                        if (mt = 0,
                        ge = null,
                        Ra(t, r, h, E),
                        l && Oa) {
                            c = 0;
                            break t
                        }
                        break;
                    default:
                        E = mt,
                        mt = 0,
                        ge = null,
                        Ra(t, r, h, E)
                    }
                }
                p0(),
                c = _t;
                break
            } catch (O) {
                Io(t, O)
            }
        while (!0);
        return e && t.shellSuspendCounter++,
        Je = Zl = null,
        rt = a,
        w.H = n,
        w.A = u,
        at === null && (bt = null,
        ut = 0,
        cu()),
        c
    }
    function p0() {
        for (; at !== null; )
            ld(at)
    }
    function b0(t, e) {
        var l = rt;
        rt |= 2;
        var a = td()
          , n = ed();
        bt !== t || ut !== e ? (Yu = null,
        Bu = se() + 500,
        Ca(t, e)) : Oa = Va(t, e);
        t: do
            try {
                if (mt !== 0 && at !== null) {
                    e = at;
                    var u = ge;
                    e: switch (mt) {
                    case 1:
                        mt = 0,
                        ge = null,
                        Ra(t, e, u, 1);
                        break;
                    case 2:
                    case 9:
                        if (or(u)) {
                            mt = 0,
                            ge = null,
                            ad(e);
                            break
                        }
                        e = function() {
                            mt !== 2 && mt !== 9 || bt !== t || (mt = 7),
                            qe(t)
                        }
                        ,
                        u.then(e, e);
                        break t;
                    case 3:
                        mt = 7;
                        break t;
                    case 4:
                        mt = 5;
                        break t;
                    case 7:
                        or(u) ? (mt = 0,
                        ge = null,
                        ad(e)) : (mt = 0,
                        ge = null,
                        Ra(t, e, u, 7));
                        break;
                    case 5:
                        var c = null;
                        switch (at.tag) {
                        case 26:
                            c = at.memoizedState;
                        case 5:
                        case 27:
                            var r = at;
                            if (c ? Xd(c) : r.stateNode.complete) {
                                mt = 0,
                                ge = null;
                                var h = r.sibling;
                                if (h !== null)
                                    at = h;
                                else {
                                    var E = r.return;
                                    E !== null ? (at = E,
                                    Xu(E)) : at = null
                                }
                                break e
                            }
                        }
                        mt = 0,
                        ge = null,
                        Ra(t, e, u, 5);
                        break;
                    case 6:
                        mt = 0,
                        ge = null,
                        Ra(t, e, u, 6);
                        break;
                    case 8:
                        us(),
                        _t = 6;
                        break t;
                    default:
                        throw Error(f(462))
                    }
                }
                S0();
                break
            } catch (O) {
                Io(t, O)
            }
        while (!0);
        return Je = Zl = null,
        w.H = a,
        w.A = n,
        rt = l,
        at !== null ? 0 : (bt = null,
        ut = 0,
        cu(),
        _t)
    }
    function S0() {
        for (; at !== null && !Zm(); )
            ld(at)
    }
    function ld(t) {
        var e = To(t.alternate, t, al);
        t.memoizedProps = t.pendingProps,
        e === null ? Xu(t) : at = e
    }
    function ad(t) {
        var e = t
          , l = e.alternate;
        switch (e.tag) {
        case 15:
        case 0:
            e = bo(l, e, e.pendingProps, e.type, void 0, ut);
            break;
        case 11:
            e = bo(l, e, e.pendingProps, e.type.render, e.ref, ut);
            break;
        case 5:
            Sc(e);
        default:
            _o(l, e),
            e = at = tr(e, al),
            e = To(l, e, al)
        }
        t.memoizedProps = t.pendingProps,
        e === null ? Xu(t) : at = e
    }
    function Ra(t, e, l, a) {
        Je = Zl = null,
        Sc(e),
        ja = null,
        fn = 0;
        var n = e.return;
        try {
            if (f0(t, n, e, l, ut)) {
                _t = 1,
                Mu(t, Se(l, t.current)),
                at = null;
                return
            }
        } catch (u) {
            if (n !== null)
                throw at = n,
                u;
            _t = 1,
            Mu(t, Se(l, t.current)),
            at = null;
            return
        }
        e.flags & 32768 ? (ct || a === 1 ? t = !0 : Oa || (ut & 536870912) !== 0 ? t = !1 : (Nl = t = !0,
        (a === 2 || a === 9 || a === 3 || a === 6) && (a = me.current,
        a !== null && a.tag === 13 && (a.flags |= 16384))),
        nd(e, t)) : Xu(e)
    }
    function Xu(t) {
        var e = t;
        do {
            if ((e.flags & 32768) !== 0) {
                nd(e, Nl);
                return
            }
            t = e.return;
            var l = d0(e.alternate, e, al);
            if (l !== null) {
                at = l;
                return
            }
            if (e = e.sibling,
            e !== null) {
                at = e;
                return
            }
            at = e = t
        } while (e !== null);
        _t === 0 && (_t = 5)
    }
    function nd(t, e) {
        do {
            var l = m0(t.alternate, t);
            if (l !== null) {
                l.flags &= 32767,
                at = l;
                return
            }
            if (l = t.return,
            l !== null && (l.flags |= 32768,
            l.subtreeFlags = 0,
            l.deletions = null),
            !e && (t = t.sibling,
            t !== null)) {
                at = t;
                return
            }
            at = t = l
        } while (t !== null);
        _t = 6,
        at = null
    }
    function ud(t, e, l, a, n, u, c, r, h) {
        t.cancelPendingCommit = null;
        do
            Qu();
        while (Yt !== 0);
        if ((rt & 6) !== 0)
            throw Error(f(327));
        if (e !== null) {
            if (e === t.current)
                throw Error(f(177));
            if (u = e.lanes | e.childLanes,
            u |= ki,
            th(t, l, u, c, r, h),
            t === bt && (at = bt = null,
            ut = 0),
            Da = e,
            zl = t,
            nl = l,
            ls = u,
            as = n,
            ko = a,
            (e.subtreeFlags & 10256) !== 0 || (e.flags & 10256) !== 0 ? (t.callbackNode = null,
            t.callbackPriority = 0,
            z0(Vn, function() {
                return rd(),
                null
            })) : (t.callbackNode = null,
            t.callbackPriority = 0),
            a = (e.flags & 13878) !== 0,
            (e.subtreeFlags & 13878) !== 0 || a) {
                a = w.T,
                w.T = null,
                n = q.p,
                q.p = 2,
                c = rt,
                rt |= 4;
                try {
                    h0(t, e, l)
                } finally {
                    rt = c,
                    q.p = n,
                    w.T = a
                }
            }
            Yt = 1,
            id(),
            cd(),
            sd()
        }
    }
    function id() {
        if (Yt === 1) {
            Yt = 0;
            var t = zl
              , e = Da
              , l = (e.flags & 13878) !== 0;
            if ((e.subtreeFlags & 13878) !== 0 || l) {
                l = w.T,
                w.T = null;
                var a = q.p;
                q.p = 2;
                var n = rt;
                rt |= 4;
                try {
                    Lo(e, t);
                    var u = vs
                      , c = Vf(t.containerInfo)
                      , r = u.focusedElem
                      , h = u.selectionRange;
                    if (c !== r && r && r.ownerDocument && Zf(r.ownerDocument.documentElement, r)) {
                        if (h !== null && Qi(r)) {
                            var E = h.start
                              , O = h.end;
                            if (O === void 0 && (O = E),
                            "selectionStart"in r)
                                r.selectionStart = E,
                                r.selectionEnd = Math.min(O, r.value.length);
                            else {
                                var C = r.ownerDocument || document
                                  , z = C && C.defaultView || window;
                                if (z.getSelection) {
                                    var A = z.getSelection()
                                      , G = r.textContent.length
                                      , k = Math.min(h.start, G)
                                      , vt = h.end === void 0 ? k : Math.min(h.end, G);
                                    !A.extend && k > vt && (c = vt,
                                    vt = k,
                                    k = c);
                                    var b = Qf(r, k)
                                      , y = Qf(r, vt);
                                    if (b && y && (A.rangeCount !== 1 || A.anchorNode !== b.node || A.anchorOffset !== b.offset || A.focusNode !== y.node || A.focusOffset !== y.offset)) {
                                        var j = C.createRange();
                                        j.setStart(b.node, b.offset),
                                        A.removeAllRanges(),
                                        k > vt ? (A.addRange(j),
                                        A.extend(y.node, y.offset)) : (j.setEnd(y.node, y.offset),
                                        A.addRange(j))
                                    }
                                }
                            }
                        }
                        for (C = [],
                        A = r; A = A.parentNode; )
                            A.nodeType === 1 && C.push({
                                element: A,
                                left: A.scrollLeft,
                                top: A.scrollTop
                            });
                        for (typeof r.focus == "function" && r.focus(),
                        r = 0; r < C.length; r++) {
                            var D = C[r];
                            D.element.scrollLeft = D.left,
                            D.element.scrollTop = D.top
                        }
                    }
                    ei = !!ys,
                    vs = ys = null
                } finally {
                    rt = n,
                    q.p = a,
                    w.T = l
                }
            }
            t.current = e,
            Yt = 2
        }
    }
    function cd() {
        if (Yt === 2) {
            Yt = 0;
            var t = zl
              , e = Da
              , l = (e.flags & 8772) !== 0;
            if ((e.subtreeFlags & 8772) !== 0 || l) {
                l = w.T,
                w.T = null;
                var a = q.p;
                q.p = 2;
                var n = rt;
                rt |= 4;
                try {
                    Uo(t, e.alternate, e)
                } finally {
                    rt = n,
                    q.p = a,
                    w.T = l
                }
            }
            Yt = 3
        }
    }
    function sd() {
        if (Yt === 4 || Yt === 3) {
            Yt = 0,
            Vm();
            var t = zl
              , e = Da
              , l = nl
              , a = ko;
            (e.subtreeFlags & 10256) !== 0 || (e.flags & 10256) !== 0 ? Yt = 5 : (Yt = 0,
            Da = zl = null,
            fd(t, t.pendingLanes));
            var n = t.pendingLanes;
            if (n === 0 && (El = null),
            Ei(l),
            e = e.stateNode,
            fe && typeof fe.onCommitFiberRoot == "function")
                try {
                    fe.onCommitFiberRoot(Za, e, void 0, (e.current.flags & 128) === 128)
                } catch {}
            if (a !== null) {
                e = w.T,
                n = q.p,
                q.p = 2,
                w.T = null;
                try {
                    for (var u = t.onRecoverableError, c = 0; c < a.length; c++) {
                        var r = a[c];
                        u(r.value, {
                            componentStack: r.stack
                        })
                    }
                } finally {
                    w.T = e,
                    q.p = n
                }
            }
            (nl & 3) !== 0 && Qu(),
            qe(t),
            n = t.pendingLanes,
            (l & 261930) !== 0 && (n & 42) !== 0 ? t === ns ? Tn++ : (Tn = 0,
            ns = t) : Tn = 0,
            An(0)
        }
    }
    function fd(t, e) {
        (t.pooledCacheLanes &= e) === 0 && (e = t.pooledCache,
        e != null && (t.pooledCache = null,
        cn(e)))
    }
    function Qu() {
        return id(),
        cd(),
        sd(),
        rd()
    }
    function rd() {
        if (Yt !== 5)
            return !1;
        var t = zl
          , e = ls;
        ls = 0;
        var l = Ei(nl)
          , a = w.T
          , n = q.p;
        try {
            q.p = 32 > l ? 32 : l,
            w.T = null,
            l = as,
            as = null;
            var u = zl
              , c = nl;
            if (Yt = 0,
            Da = zl = null,
            nl = 0,
            (rt & 6) !== 0)
                throw Error(f(331));
            var r = rt;
            if (rt |= 4,
            Vo(u.current),
            Xo(u, u.current, c, l),
            rt = r,
            An(0, !1),
            fe && typeof fe.onPostCommitFiberRoot == "function")
                try {
                    fe.onPostCommitFiberRoot(Za, u)
                } catch {}
            return !0
        } finally {
            q.p = n,
            w.T = a,
            fd(t, e)
        }
    }
    function od(t, e, l) {
        e = Se(l, e),
        e = Hc(t.stateNode, e, 2),
        t = vl(t, e, 2),
        t !== null && (Ka(t, 2),
        qe(t))
    }
    function ht(t, e, l) {
        if (t.tag === 3)
            od(t, t, l);
        else
            for (; e !== null; ) {
                if (e.tag === 3) {
                    od(e, t, l);
                    break
                } else if (e.tag === 1) {
                    var a = e.stateNode;
                    if (typeof e.type.getDerivedStateFromError == "function" || typeof a.componentDidCatch == "function" && (El === null || !El.has(a))) {
                        t = Se(l, t),
                        l = oo(2),
                        a = vl(e, l, 2),
                        a !== null && (mo(l, a, e, t),
                        Ka(a, 2),
                        qe(a));
                        break
                    }
                }
                e = e.return
            }
    }
    function cs(t, e, l) {
        var a = t.pingCache;
        if (a === null) {
            a = t.pingCache = new y0;
            var n = new Set;
            a.set(e, n)
        } else
            n = a.get(e),
            n === void 0 && (n = new Set,
            a.set(e, n));
        n.has(l) || (Pc = !0,
        n.add(l),
        t = N0.bind(null, t, e, l),
        e.then(t, t))
    }
    function N0(t, e, l) {
        var a = t.pingCache;
        a !== null && a.delete(e),
        t.pingedLanes |= t.suspendedLanes & l,
        t.warmLanes &= ~l,
        bt === t && (ut & l) === l && (_t === 4 || _t === 3 && (ut & 62914560) === ut && 300 > se() - qu ? (rt & 2) === 0 && Ca(t, 0) : ts |= l,
        wa === ut && (wa = 0)),
        qe(t)
    }
    function dd(t, e) {
        e === 0 && (e = nf()),
        t = Gl(t, e),
        t !== null && (Ka(t, e),
        qe(t))
    }
    function j0(t) {
        var e = t.memoizedState
          , l = 0;
        e !== null && (l = e.retryLane),
        dd(t, l)
    }
    function E0(t, e) {
        var l = 0;
        switch (t.tag) {
        case 31:
        case 13:
            var a = t.stateNode
              , n = t.memoizedState;
            n !== null && (l = n.retryLane);
            break;
        case 19:
            a = t.stateNode;
            break;
        case 22:
            a = t.stateNode._retryCache;
            break;
        default:
            throw Error(f(314))
        }
        a !== null && a.delete(e),
        dd(t, l)
    }
    function z0(t, e) {
        return bi(t, e)
    }
    var Zu = null
      , Ua = null
      , ss = !1
      , Vu = !1
      , fs = !1
      , Al = 0;
    function qe(t) {
        t !== Ua && t.next === null && (Ua === null ? Zu = Ua = t : Ua = Ua.next = t),
        Vu = !0,
        ss || (ss = !0,
        A0())
    }
    function An(t, e) {
        if (!fs && Vu) {
            fs = !0;
            do
                for (var l = !1, a = Zu; a !== null; ) {
                    if (t !== 0) {
                        var n = a.pendingLanes;
                        if (n === 0)
                            var u = 0;
                        else {
                            var c = a.suspendedLanes
                              , r = a.pingedLanes;
                            u = (1 << 31 - re(42 | t) + 1) - 1,
                            u &= n & ~(c & ~r),
                            u = u & 201326741 ? u & 201326741 | 1 : u ? u | 2 : 0
                        }
                        u !== 0 && (l = !0,
                        xd(a, u))
                    } else
                        u = ut,
                        u = $n(a, a === bt ? u : 0, a.cancelPendingCommit !== null || a.timeoutHandle !== -1),
                        (u & 3) === 0 || Va(a, u) || (l = !0,
                        xd(a, u));
                    a = a.next
                }
            while (l);
            fs = !1
        }
    }
    function T0() {
        md()
    }
    function md() {
        Vu = ss = !1;
        var t = 0;
        Al !== 0 && q0() && (t = Al);
        for (var e = se(), l = null, a = Zu; a !== null; ) {
            var n = a.next
              , u = hd(a, e);
            u === 0 ? (a.next = null,
            l === null ? Zu = n : l.next = n,
            n === null && (Ua = l)) : (l = a,
            (t !== 0 || (u & 3) !== 0) && (Vu = !0)),
            a = n
        }
        Yt !== 0 && Yt !== 5 || An(t),
        Al !== 0 && (Al = 0)
    }
    function hd(t, e) {
        for (var l = t.suspendedLanes, a = t.pingedLanes, n = t.expirationTimes, u = t.pendingLanes & -62914561; 0 < u; ) {
            var c = 31 - re(u)
              , r = 1 << c
              , h = n[c];
            h === -1 ? ((r & l) === 0 || (r & a) !== 0) && (n[c] = Pm(r, e)) : h <= e && (t.expiredLanes |= r),
            u &= ~r
        }
        if (e = bt,
        l = ut,
        l = $n(t, t === e ? l : 0, t.cancelPendingCommit !== null || t.timeoutHandle !== -1),
        a = t.callbackNode,
        l === 0 || t === e && (mt === 2 || mt === 9) || t.cancelPendingCommit !== null)
            return a !== null && a !== null && Si(a),
            t.callbackNode = null,
            t.callbackPriority = 0;
        if ((l & 3) === 0 || Va(t, l)) {
            if (e = l & -l,
            e === t.callbackPriority)
                return e;
            switch (a !== null && Si(a),
            Ei(l)) {
            case 2:
            case 8:
                l = lf;
                break;
            case 32:
                l = Vn;
                break;
            case 268435456:
                l = af;
                break;
            default:
                l = Vn
            }
            return a = gd.bind(null, t),
            l = bi(l, a),
            t.callbackPriority = e,
            t.callbackNode = l,
            e
        }
        return a !== null && a !== null && Si(a),
        t.callbackPriority = 2,
        t.callbackNode = null,
        2
    }
    function gd(t, e) {
        if (Yt !== 0 && Yt !== 5)
            return t.callbackNode = null,
            t.callbackPriority = 0,
            null;
        var l = t.callbackNode;
        if (Qu() && t.callbackNode !== l)
            return null;
        var a = ut;
        return a = $n(t, t === bt ? a : 0, t.cancelPendingCommit !== null || t.timeoutHandle !== -1),
        a === 0 ? null : (Wo(t, a, e),
        hd(t, se()),
        t.callbackNode != null && t.callbackNode === l ? gd.bind(null, t) : null)
    }
    function xd(t, e) {
        if (Qu())
            return null;
        Wo(t, e, !0)
    }
    function A0() {
        Y0(function() {
            (rt & 6) !== 0 ? bi(ef, T0) : md()
        })
    }
    function rs() {
        if (Al === 0) {
            var t = ba;
            t === 0 && (t = Kn,
            Kn <<= 1,
            (Kn & 261888) === 0 && (Kn = 256)),
            Al = t
        }
        return Al
    }
    function yd(t) {
        return t == null || typeof t == "symbol" || typeof t == "boolean" ? null : typeof t == "function" ? t : Pn("" + t)
    }
    function vd(t, e) {
        var l = e.ownerDocument.createElement("input");
        return l.name = e.name,
        l.value = e.value,
        t.id && l.setAttribute("form", t.id),
        e.parentNode.insertBefore(l, e),
        t = new FormData(t),
        l.parentNode.removeChild(l),
        t
    }
    function _0(t, e, l, a, n) {
        if (e === "submit" && l && l.stateNode === n) {
            var u = yd((n[It] || null).action)
              , c = a.submitter;
            c && (e = (e = c[It] || null) ? yd(e.formAction) : c.getAttribute("formAction"),
            e !== null && (u = e,
            c = null));
            var r = new au("action","action",null,a,n);
            t.push({
                event: r,
                listeners: [{
                    instance: null,
                    listener: function() {
                        if (a.defaultPrevented) {
                            if (Al !== 0) {
                                var h = c ? vd(n, c) : new FormData(n);
                                Oc(l, {
                                    pending: !0,
                                    data: h,
                                    method: n.method,
                                    action: u
                                }, null, h)
                            }
                        } else
                            typeof u == "function" && (r.preventDefault(),
                            h = c ? vd(n, c) : new FormData(n),
                            Oc(l, {
                                pending: !0,
                                data: h,
                                method: n.method,
                                action: u
                            }, u, h))
                    },
                    currentTarget: n
                }]
            })
        }
    }
    for (var os = 0; os < Ji.length; os++) {
        var ds = Ji[os]
          , M0 = ds.toLowerCase()
          , O0 = ds[0].toUpperCase() + ds.slice(1);
        Oe(M0, "on" + O0)
    }
    Oe(kf, "onAnimationEnd"),
    Oe($f, "onAnimationIteration"),
    Oe(Wf, "onAnimationStart"),
    Oe("dblclick", "onDoubleClick"),
    Oe("focusin", "onFocus"),
    Oe("focusout", "onBlur"),
    Oe(Kh, "onTransitionRun"),
    Oe(Jh, "onTransitionStart"),
    Oe(kh, "onTransitionCancel"),
    Oe(Ff, "onTransitionEnd"),
    ia("onMouseEnter", ["mouseout", "mouseover"]),
    ia("onMouseLeave", ["mouseout", "mouseover"]),
    ia("onPointerEnter", ["pointerout", "pointerover"]),
    ia("onPointerLeave", ["pointerout", "pointerover"]),
    ql("onChange", "change click focusin focusout input keydown keyup selectionchange".split(" ")),
    ql("onSelect", "focusout contextmenu dragend focusin keydown keyup mousedown mouseup selectionchange".split(" ")),
    ql("onBeforeInput", ["compositionend", "keypress", "textInput", "paste"]),
    ql("onCompositionEnd", "compositionend focusout keydown keypress keyup mousedown".split(" ")),
    ql("onCompositionStart", "compositionstart focusout keydown keypress keyup mousedown".split(" ")),
    ql("onCompositionUpdate", "compositionupdate focusout keydown keypress keyup mousedown".split(" "));
    var _n = "abort canplay canplaythrough durationchange emptied encrypted ended error loadeddata loadedmetadata loadstart pause play playing progress ratechange resize seeked seeking stalled suspend timeupdate volumechange waiting".split(" ")
      , w0 = new Set("beforetoggle cancel close invalid load scroll scrollend toggle".split(" ").concat(_n));
    function pd(t, e) {
        e = (e & 4) !== 0;
        for (var l = 0; l < t.length; l++) {
            var a = t[l]
              , n = a.event;
            a = a.listeners;
            t: {
                var u = void 0;
                if (e)
                    for (var c = a.length - 1; 0 <= c; c--) {
                        var r = a[c]
                          , h = r.instance
                          , E = r.currentTarget;
                        if (r = r.listener,
                        h !== u && n.isPropagationStopped())
                            break t;
                        u = r,
                        n.currentTarget = E;
                        try {
                            u(n)
                        } catch (O) {
                            iu(O)
                        }
                        n.currentTarget = null,
                        u = h
                    }
                else
                    for (c = 0; c < a.length; c++) {
                        if (r = a[c],
                        h = r.instance,
                        E = r.currentTarget,
                        r = r.listener,
                        h !== u && n.isPropagationStopped())
                            break t;
                        u = r,
                        n.currentTarget = E;
                        try {
                            u(n)
                        } catch (O) {
                            iu(O)
                        }
                        n.currentTarget = null,
                        u = h
                    }
            }
        }
    }
    function nt(t, e) {
        var l = e[zi];
        l === void 0 && (l = e[zi] = new Set);
        var a = t + "__bubble";
        l.has(a) || (bd(e, t, 2, !1),
        l.add(a))
    }
    function ms(t, e, l) {
        var a = 0;
        e && (a |= 4),
        bd(l, t, a, e)
    }
    var Ku = "_reactListening" + Math.random().toString(36).slice(2);
    function hs(t) {
        if (!t[Ku]) {
            t[Ku] = !0,
            df.forEach(function(l) {
                l !== "selectionchange" && (w0.has(l) || ms(l, !1, t),
                ms(l, !0, t))
            });
            var e = t.nodeType === 9 ? t : t.ownerDocument;
            e === null || e[Ku] || (e[Ku] = !0,
            ms("selectionchange", !1, e))
        }
    }
    function bd(t, e, l, a) {
        switch ($d(e)) {
        case 2:
            var n = ug;
            break;
        case 8:
            n = ig;
            break;
        default:
            n = Ms
        }
        l = n.bind(null, e, l, t),
        n = void 0,
        !Ri || e !== "touchstart" && e !== "touchmove" && e !== "wheel" || (n = !0),
        a ? n !== void 0 ? t.addEventListener(e, l, {
            capture: !0,
            passive: n
        }) : t.addEventListener(e, l, !0) : n !== void 0 ? t.addEventListener(e, l, {
            passive: n
        }) : t.addEventListener(e, l, !1)
    }
    function gs(t, e, l, a, n) {
        var u = a;
        if ((e & 1) === 0 && (e & 2) === 0 && a !== null)
            t: for (; ; ) {
                if (a === null)
                    return;
                var c = a.tag;
                if (c === 3 || c === 4) {
                    var r = a.stateNode.containerInfo;
                    if (r === n)
                        break;
                    if (c === 4)
                        for (c = a.return; c !== null; ) {
                            var h = c.tag;
                            if ((h === 3 || h === 4) && c.stateNode.containerInfo === n)
                                return;
                            c = c.return
                        }
                    for (; r !== null; ) {
                        if (c = aa(r),
                        c === null)
                            return;
                        if (h = c.tag,
                        h === 5 || h === 6 || h === 26 || h === 27) {
                            a = u = c;
                            continue t
                        }
                        r = r.parentNode
                    }
                }
                a = a.return
            }
        Ef(function() {
            var E = u
              , O = Di(l)
              , C = [];
            t: {
                var z = If.get(t);
                if (z !== void 0) {
                    var A = au
                      , G = t;
                    switch (t) {
                    case "keypress":
                        if (eu(l) === 0)
                            break t;
                    case "keydown":
                    case "keyup":
                        A = Eh;
                        break;
                    case "focusin":
                        G = "focus",
                        A = Bi;
                        break;
                    case "focusout":
                        G = "blur",
                        A = Bi;
                        break;
                    case "beforeblur":
                    case "afterblur":
                        A = Bi;
                        break;
                    case "click":
                        if (l.button === 2)
                            break t;
                    case "auxclick":
                    case "dblclick":
                    case "mousedown":
                    case "mousemove":
                    case "mouseup":
                    case "mouseout":
                    case "mouseover":
                    case "contextmenu":
                        A = Af;
                        break;
                    case "drag":
                    case "dragend":
                    case "dragenter":
                    case "dragexit":
                    case "dragleave":
                    case "dragover":
                    case "dragstart":
                    case "drop":
                        A = dh;
                        break;
                    case "touchcancel":
                    case "touchend":
                    case "touchmove":
                    case "touchstart":
                        A = Ah;
                        break;
                    case kf:
                    case $f:
                    case Wf:
                        A = gh;
                        break;
                    case Ff:
                        A = Mh;
                        break;
                    case "scroll":
                    case "scrollend":
                        A = rh;
                        break;
                    case "wheel":
                        A = wh;
                        break;
                    case "copy":
                    case "cut":
                    case "paste":
                        A = yh;
                        break;
                    case "gotpointercapture":
                    case "lostpointercapture":
                    case "pointercancel":
                    case "pointerdown":
                    case "pointermove":
                    case "pointerout":
                    case "pointerover":
                    case "pointerup":
                        A = Mf;
                        break;
                    case "toggle":
                    case "beforetoggle":
                        A = Ch
                    }
                    var k = (e & 4) !== 0
                      , vt = !k && (t === "scroll" || t === "scrollend")
                      , b = k ? z !== null ? z + "Capture" : null : z;
                    k = [];
                    for (var y = E, j; y !== null; ) {
                        var D = y;
                        if (j = D.stateNode,
                        D = D.tag,
                        D !== 5 && D !== 26 && D !== 27 || j === null || b === null || (D = $a(y, b),
                        D != null && k.push(Mn(y, D, j))),
                        vt)
                            break;
                        y = y.return
                    }
                    0 < k.length && (z = new A(z,G,null,l,O),
                    C.push({
                        event: z,
                        listeners: k
                    }))
                }
            }
            if ((e & 7) === 0) {
                t: {
                    if (z = t === "mouseover" || t === "pointerover",
                    A = t === "mouseout" || t === "pointerout",
                    z && l !== wi && (G = l.relatedTarget || l.fromElement) && (aa(G) || G[la]))
                        break t;
                    if ((A || z) && (z = O.window === O ? O : (z = O.ownerDocument) ? z.defaultView || z.parentWindow : window,
                    A ? (G = l.relatedTarget || l.toElement,
                    A = E,
                    G = G ? aa(G) : null,
                    G !== null && (vt = g(G),
                    k = G.tag,
                    G !== vt || k !== 5 && k !== 27 && k !== 6) && (G = null)) : (A = null,
                    G = E),
                    A !== G)) {
                        if (k = Af,
                        D = "onMouseLeave",
                        b = "onMouseEnter",
                        y = "mouse",
                        (t === "pointerout" || t === "pointerover") && (k = Mf,
                        D = "onPointerLeave",
                        b = "onPointerEnter",
                        y = "pointer"),
                        vt = A == null ? z : ka(A),
                        j = G == null ? z : ka(G),
                        z = new k(D,y + "leave",A,l,O),
                        z.target = vt,
                        z.relatedTarget = j,
                        D = null,
                        aa(O) === E && (k = new k(b,y + "enter",G,l,O),
                        k.target = j,
                        k.relatedTarget = vt,
                        D = k),
                        vt = D,
                        A && G)
                            e: {
                                for (k = D0,
                                b = A,
                                y = G,
                                j = 0,
                                D = b; D; D = k(D))
                                    j++;
                                D = 0;
                                for (var K = y; K; K = k(K))
                                    D++;
                                for (; 0 < j - D; )
                                    b = k(b),
                                    j--;
                                for (; 0 < D - j; )
                                    y = k(y),
                                    D--;
                                for (; j--; ) {
                                    if (b === y || y !== null && b === y.alternate) {
                                        k = b;
                                        break e
                                    }
                                    b = k(b),
                                    y = k(y)
                                }
                                k = null
                            }
                        else
                            k = null;
                        A !== null && Sd(C, z, A, k, !1),
                        G !== null && vt !== null && Sd(C, vt, G, k, !0)
                    }
                }
                t: {
                    if (z = E ? ka(E) : window,
                    A = z.nodeName && z.nodeName.toLowerCase(),
                    A === "select" || A === "input" && z.type === "file")
                        var st = qf;
                    else if (Uf(z))
                        if (Bf)
                            st = Qh;
                        else {
                            st = Gh;
                            var V = Lh
                        }
                    else
                        A = z.nodeName,
                        !A || A.toLowerCase() !== "input" || z.type !== "checkbox" && z.type !== "radio" ? E && Oi(E.elementType) && (st = qf) : st = Xh;
                    if (st && (st = st(t, E))) {
                        Hf(C, st, l, O);
                        break t
                    }
                    V && V(t, z, E),
                    t === "focusout" && E && z.type === "number" && E.memoizedProps.value != null && Mi(z, "number", z.value)
                }
                switch (V = E ? ka(E) : window,
                t) {
                case "focusin":
                    (Uf(V) || V.contentEditable === "true") && (da = V,
                    Zi = E,
                    an = null);
                    break;
                case "focusout":
                    an = Zi = da = null;
                    break;
                case "mousedown":
                    Vi = !0;
                    break;
                case "contextmenu":
                case "mouseup":
                case "dragend":
                    Vi = !1,
                    Kf(C, l, O);
                    break;
                case "selectionchange":
                    if (Vh)
                        break;
                case "keydown":
                case "keyup":
                    Kf(C, l, O)
                }
                var tt;
                if (Li)
                    t: {
                        switch (t) {
                        case "compositionstart":
                            var it = "onCompositionStart";
                            break t;
                        case "compositionend":
                            it = "onCompositionEnd";
                            break t;
                        case "compositionupdate":
                            it = "onCompositionUpdate";
                            break t
                        }
                        it = void 0
                    }
                else
                    oa ? Cf(t, l) && (it = "onCompositionEnd") : t === "keydown" && l.keyCode === 229 && (it = "onCompositionStart");
                it && (Of && l.locale !== "ko" && (oa || it !== "onCompositionStart" ? it === "onCompositionEnd" && oa && (tt = zf()) : (ol = O,
                Ui = "value"in ol ? ol.value : ol.textContent,
                oa = !0)),
                V = Ju(E, it),
                0 < V.length && (it = new _f(it,t,null,l,O),
                C.push({
                    event: it,
                    listeners: V
                }),
                tt ? it.data = tt : (tt = Rf(l),
                tt !== null && (it.data = tt)))),
                (tt = Uh ? Hh(t, l) : qh(t, l)) && (it = Ju(E, "onBeforeInput"),
                0 < it.length && (V = new _f("onBeforeInput","beforeinput",null,l,O),
                C.push({
                    event: V,
                    listeners: it
                }),
                V.data = tt)),
                _0(C, t, E, l, O)
            }
            pd(C, e)
        })
    }
    function Mn(t, e, l) {
        return {
            instance: t,
            listener: e,
            currentTarget: l
        }
    }
    function Ju(t, e) {
        for (var l = e + "Capture", a = []; t !== null; ) {
            var n = t
              , u = n.stateNode;
            if (n = n.tag,
            n !== 5 && n !== 26 && n !== 27 || u === null || (n = $a(t, l),
            n != null && a.unshift(Mn(t, n, u)),
            n = $a(t, e),
            n != null && a.push(Mn(t, n, u))),
            t.tag === 3)
                return a;
            t = t.return
        }
        return []
    }
    function D0(t) {
        if (t === null)
            return null;
        do
            t = t.return;
        while (t && t.tag !== 5 && t.tag !== 27);
        return t || null
    }
    function Sd(t, e, l, a, n) {
        for (var u = e._reactName, c = []; l !== null && l !== a; ) {
            var r = l
              , h = r.alternate
              , E = r.stateNode;
            if (r = r.tag,
            h !== null && h === a)
                break;
            r !== 5 && r !== 26 && r !== 27 || E === null || (h = E,
            n ? (E = $a(l, u),
            E != null && c.unshift(Mn(l, E, h))) : n || (E = $a(l, u),
            E != null && c.push(Mn(l, E, h)))),
            l = l.return
        }
        c.length !== 0 && t.push({
            event: e,
            listeners: c
        })
    }
    var C0 = /\r\n?/g
      , R0 = /\u0000|\uFFFD/g;
    function Nd(t) {
        return (typeof t == "string" ? t : "" + t).replace(C0, `
`).replace(R0, "")
    }
    function jd(t, e) {
        return e = Nd(e),
        Nd(t) === e
    }
    function yt(t, e, l, a, n, u) {
        switch (l) {
        case "children":
            typeof a == "string" ? e === "body" || e === "textarea" && a === "" || sa(t, a) : (typeof a == "number" || typeof a == "bigint") && e !== "body" && sa(t, "" + a);
            break;
        case "className":
            Fn(t, "class", a);
            break;
        case "tabIndex":
            Fn(t, "tabindex", a);
            break;
        case "dir":
        case "role":
        case "viewBox":
        case "width":
        case "height":
            Fn(t, l, a);
            break;
        case "style":
            Nf(t, a, u);
            break;
        case "data":
            if (e !== "object") {
                Fn(t, "data", a);
                break
            }
        case "src":
        case "href":
            if (a === "" && (e !== "a" || l !== "href")) {
                t.removeAttribute(l);
                break
            }
            if (a == null || typeof a == "function" || typeof a == "symbol" || typeof a == "boolean") {
                t.removeAttribute(l);
                break
            }
            a = Pn("" + a),
            t.setAttribute(l, a);
            break;
        case "action":
        case "formAction":
            if (typeof a == "function") {
                t.setAttribute(l, "javascript:throw new Error('A React form was unexpectedly submitted. If you called form.submit() manually, consider using form.requestSubmit() instead. If you\\'re trying to use event.stopPropagation() in a submit event handler, consider also calling event.preventDefault().')");
                break
            } else
                typeof u == "function" && (l === "formAction" ? (e !== "input" && yt(t, e, "name", n.name, n, null),
                yt(t, e, "formEncType", n.formEncType, n, null),
                yt(t, e, "formMethod", n.formMethod, n, null),
                yt(t, e, "formTarget", n.formTarget, n, null)) : (yt(t, e, "encType", n.encType, n, null),
                yt(t, e, "method", n.method, n, null),
                yt(t, e, "target", n.target, n, null)));
            if (a == null || typeof a == "symbol" || typeof a == "boolean") {
                t.removeAttribute(l);
                break
            }
            a = Pn("" + a),
            t.setAttribute(l, a);
            break;
        case "onClick":
            a != null && (t.onclick = Qe);
            break;
        case "onScroll":
            a != null && nt("scroll", t);
            break;
        case "onScrollEnd":
            a != null && nt("scrollend", t);
            break;
        case "dangerouslySetInnerHTML":
            if (a != null) {
                if (typeof a != "object" || !("__html"in a))
                    throw Error(f(61));
                if (l = a.__html,
                l != null) {
                    if (n.children != null)
                        throw Error(f(60));
                    t.innerHTML = l
                }
            }
            break;
        case "multiple":
            t.multiple = a && typeof a != "function" && typeof a != "symbol";
            break;
        case "muted":
            t.muted = a && typeof a != "function" && typeof a != "symbol";
            break;
        case "suppressContentEditableWarning":
        case "suppressHydrationWarning":
        case "defaultValue":
        case "defaultChecked":
        case "innerHTML":
        case "ref":
            break;
        case "autoFocus":
            break;
        case "xlinkHref":
            if (a == null || typeof a == "function" || typeof a == "boolean" || typeof a == "symbol") {
                t.removeAttribute("xlink:href");
                break
            }
            l = Pn("" + a),
            t.setAttributeNS("http://www.w3.org/1999/xlink", "xlink:href", l);
            break;
        case "contentEditable":
        case "spellCheck":
        case "draggable":
        case "value":
        case "autoReverse":
        case "externalResourcesRequired":
        case "focusable":
        case "preserveAlpha":
            a != null && typeof a != "function" && typeof a != "symbol" ? t.setAttribute(l, "" + a) : t.removeAttribute(l);
            break;
        case "inert":
        case "allowFullScreen":
        case "async":
        case "autoPlay":
        case "controls":
        case "default":
        case "defer":
        case "disabled":
        case "disablePictureInPicture":
        case "disableRemotePlayback":
        case "formNoValidate":
        case "hidden":
        case "loop":
        case "noModule":
        case "noValidate":
        case "open":
        case "playsInline":
        case "readOnly":
        case "required":
        case "reversed":
        case "scoped":
        case "seamless":
        case "itemScope":
            a && typeof a != "function" && typeof a != "symbol" ? t.setAttribute(l, "") : t.removeAttribute(l);
            break;
        case "capture":
        case "download":
            a === !0 ? t.setAttribute(l, "") : a !== !1 && a != null && typeof a != "function" && typeof a != "symbol" ? t.setAttribute(l, a) : t.removeAttribute(l);
            break;
        case "cols":
        case "rows":
        case "size":
        case "span":
            a != null && typeof a != "function" && typeof a != "symbol" && !isNaN(a) && 1 <= a ? t.setAttribute(l, a) : t.removeAttribute(l);
            break;
        case "rowSpan":
        case "start":
            a == null || typeof a == "function" || typeof a == "symbol" || isNaN(a) ? t.removeAttribute(l) : t.setAttribute(l, a);
            break;
        case "popover":
            nt("beforetoggle", t),
            nt("toggle", t),
            Wn(t, "popover", a);
            break;
        case "xlinkActuate":
            Xe(t, "http://www.w3.org/1999/xlink", "xlink:actuate", a);
            break;
        case "xlinkArcrole":
            Xe(t, "http://www.w3.org/1999/xlink", "xlink:arcrole", a);
            break;
        case "xlinkRole":
            Xe(t, "http://www.w3.org/1999/xlink", "xlink:role", a);
            break;
        case "xlinkShow":
            Xe(t, "http://www.w3.org/1999/xlink", "xlink:show", a);
            break;
        case "xlinkTitle":
            Xe(t, "http://www.w3.org/1999/xlink", "xlink:title", a);
            break;
        case "xlinkType":
            Xe(t, "http://www.w3.org/1999/xlink", "xlink:type", a);
            break;
        case "xmlBase":
            Xe(t, "http://www.w3.org/XML/1998/namespace", "xml:base", a);
            break;
        case "xmlLang":
            Xe(t, "http://www.w3.org/XML/1998/namespace", "xml:lang", a);
            break;
        case "xmlSpace":
            Xe(t, "http://www.w3.org/XML/1998/namespace", "xml:space", a);
            break;
        case "is":
            Wn(t, "is", a);
            break;
        case "innerText":
        case "textContent":
            break;
        default:
            (!(2 < l.length) || l[0] !== "o" && l[0] !== "O" || l[1] !== "n" && l[1] !== "N") && (l = sh.get(l) || l,
            Wn(t, l, a))
        }
    }
    function xs(t, e, l, a, n, u) {
        switch (l) {
        case "style":
            Nf(t, a, u);
            break;
        case "dangerouslySetInnerHTML":
            if (a != null) {
                if (typeof a != "object" || !("__html"in a))
                    throw Error(f(61));
                if (l = a.__html,
                l != null) {
                    if (n.children != null)
                        throw Error(f(60));
                    t.innerHTML = l
                }
            }
            break;
        case "children":
            typeof a == "string" ? sa(t, a) : (typeof a == "number" || typeof a == "bigint") && sa(t, "" + a);
            break;
        case "onScroll":
            a != null && nt("scroll", t);
            break;
        case "onScrollEnd":
            a != null && nt("scrollend", t);
            break;
        case "onClick":
            a != null && (t.onclick = Qe);
            break;
        case "suppressContentEditableWarning":
        case "suppressHydrationWarning":
        case "innerHTML":
        case "ref":
            break;
        case "innerText":
        case "textContent":
            break;
        default:
            if (!mf.hasOwnProperty(l))
                t: {
                    if (l[0] === "o" && l[1] === "n" && (n = l.endsWith("Capture"),
                    e = l.slice(2, n ? l.length - 7 : void 0),
                    u = t[It] || null,
                    u = u != null ? u[l] : null,
                    typeof u == "function" && t.removeEventListener(e, u, n),
                    typeof a == "function")) {
                        typeof u != "function" && u !== null && (l in t ? t[l] = null : t.hasAttribute(l) && t.removeAttribute(l)),
                        t.addEventListener(e, a, n);
                        break t
                    }
                    l in t ? t[l] = a : a === !0 ? t.setAttribute(l, "") : Wn(t, l, a)
                }
        }
    }
    function Jt(t, e, l) {
        switch (e) {
        case "div":
        case "span":
        case "svg":
        case "path":
        case "a":
        case "g":
        case "p":
        case "li":
            break;
        case "img":
            nt("error", t),
            nt("load", t);
            var a = !1, n = !1, u;
            for (u in l)
                if (l.hasOwnProperty(u)) {
                    var c = l[u];
                    if (c != null)
                        switch (u) {
                        case "src":
                            a = !0;
                            break;
                        case "srcSet":
                            n = !0;
                            break;
                        case "children":
                        case "dangerouslySetInnerHTML":
                            throw Error(f(137, e));
                        default:
                            yt(t, e, u, c, l, null)
                        }
                }
            n && yt(t, e, "srcSet", l.srcSet, l, null),
            a && yt(t, e, "src", l.src, l, null);
            return;
        case "input":
            nt("invalid", t);
            var r = u = c = n = null
              , h = null
              , E = null;
            for (a in l)
                if (l.hasOwnProperty(a)) {
                    var O = l[a];
                    if (O != null)
                        switch (a) {
                        case "name":
                            n = O;
                            break;
                        case "type":
                            c = O;
                            break;
                        case "checked":
                            h = O;
                            break;
                        case "defaultChecked":
                            E = O;
                            break;
                        case "value":
                            u = O;
                            break;
                        case "defaultValue":
                            r = O;
                            break;
                        case "children":
                        case "dangerouslySetInnerHTML":
                            if (O != null)
                                throw Error(f(137, e));
                            break;
                        default:
                            yt(t, e, a, O, l, null)
                        }
                }
            vf(t, u, r, h, E, c, n, !1);
            return;
        case "select":
            nt("invalid", t),
            a = c = u = null;
            for (n in l)
                if (l.hasOwnProperty(n) && (r = l[n],
                r != null))
                    switch (n) {
                    case "value":
                        u = r;
                        break;
                    case "defaultValue":
                        c = r;
                        break;
                    case "multiple":
                        a = r;
                    default:
                        yt(t, e, n, r, l, null)
                    }
            e = u,
            l = c,
            t.multiple = !!a,
            e != null ? ca(t, !!a, e, !1) : l != null && ca(t, !!a, l, !0);
            return;
        case "textarea":
            nt("invalid", t),
            u = n = a = null;
            for (c in l)
                if (l.hasOwnProperty(c) && (r = l[c],
                r != null))
                    switch (c) {
                    case "value":
                        a = r;
                        break;
                    case "defaultValue":
                        n = r;
                        break;
                    case "children":
                        u = r;
                        break;
                    case "dangerouslySetInnerHTML":
                        if (r != null)
                            throw Error(f(91));
                        break;
                    default:
                        yt(t, e, c, r, l, null)
                    }
            bf(t, a, n, u);
            return;
        case "option":
            for (h in l)
                if (l.hasOwnProperty(h) && (a = l[h],
                a != null))
                    switch (h) {
                    case "selected":
                        t.selected = a && typeof a != "function" && typeof a != "symbol";
                        break;
                    default:
                        yt(t, e, h, a, l, null)
                    }
            return;
        case "dialog":
            nt("beforetoggle", t),
            nt("toggle", t),
            nt("cancel", t),
            nt("close", t);
            break;
        case "iframe":
        case "object":
            nt("load", t);
            break;
        case "video":
        case "audio":
            for (a = 0; a < _n.length; a++)
                nt(_n[a], t);
            break;
        case "image":
            nt("error", t),
            nt("load", t);
            break;
        case "details":
            nt("toggle", t);
            break;
        case "embed":
        case "source":
        case "link":
            nt("error", t),
            nt("load", t);
        case "area":
        case "base":
        case "br":
        case "col":
        case "hr":
        case "keygen":
        case "meta":
        case "param":
        case "track":
        case "wbr":
        case "menuitem":
            for (E in l)
                if (l.hasOwnProperty(E) && (a = l[E],
                a != null))
                    switch (E) {
                    case "children":
                    case "dangerouslySetInnerHTML":
                        throw Error(f(137, e));
                    default:
                        yt(t, e, E, a, l, null)
                    }
            return;
        default:
            if (Oi(e)) {
                for (O in l)
                    l.hasOwnProperty(O) && (a = l[O],
                    a !== void 0 && xs(t, e, O, a, l, void 0));
                return
            }
        }
        for (r in l)
            l.hasOwnProperty(r) && (a = l[r],
            a != null && yt(t, e, r, a, l, null))
    }
    function U0(t, e, l, a) {
        switch (e) {
        case "div":
        case "span":
        case "svg":
        case "path":
        case "a":
        case "g":
        case "p":
        case "li":
            break;
        case "input":
            var n = null
              , u = null
              , c = null
              , r = null
              , h = null
              , E = null
              , O = null;
            for (A in l) {
                var C = l[A];
                if (l.hasOwnProperty(A) && C != null)
                    switch (A) {
                    case "checked":
                        break;
                    case "value":
                        break;
                    case "defaultValue":
                        h = C;
                    default:
                        a.hasOwnProperty(A) || yt(t, e, A, null, a, C)
                    }
            }
            for (var z in a) {
                var A = a[z];
                if (C = l[z],
                a.hasOwnProperty(z) && (A != null || C != null))
                    switch (z) {
                    case "type":
                        u = A;
                        break;
                    case "name":
                        n = A;
                        break;
                    case "checked":
                        E = A;
                        break;
                    case "defaultChecked":
                        O = A;
                        break;
                    case "value":
                        c = A;
                        break;
                    case "defaultValue":
                        r = A;
                        break;
                    case "children":
                    case "dangerouslySetInnerHTML":
                        if (A != null)
                            throw Error(f(137, e));
                        break;
                    default:
                        A !== C && yt(t, e, z, A, a, C)
                    }
            }
            _i(t, c, r, h, E, O, u, n);
            return;
        case "select":
            A = c = r = z = null;
            for (u in l)
                if (h = l[u],
                l.hasOwnProperty(u) && h != null)
                    switch (u) {
                    case "value":
                        break;
                    case "multiple":
                        A = h;
                    default:
                        a.hasOwnProperty(u) || yt(t, e, u, null, a, h)
                    }
            for (n in a)
                if (u = a[n],
                h = l[n],
                a.hasOwnProperty(n) && (u != null || h != null))
                    switch (n) {
                    case "value":
                        z = u;
                        break;
                    case "defaultValue":
                        r = u;
                        break;
                    case "multiple":
                        c = u;
                    default:
                        u !== h && yt(t, e, n, u, a, h)
                    }
            e = r,
            l = c,
            a = A,
            z != null ? ca(t, !!l, z, !1) : !!a != !!l && (e != null ? ca(t, !!l, e, !0) : ca(t, !!l, l ? [] : "", !1));
            return;
        case "textarea":
            A = z = null;
            for (r in l)
                if (n = l[r],
                l.hasOwnProperty(r) && n != null && !a.hasOwnProperty(r))
                    switch (r) {
                    case "value":
                        break;
                    case "children":
                        break;
                    default:
                        yt(t, e, r, null, a, n)
                    }
            for (c in a)
                if (n = a[c],
                u = l[c],
                a.hasOwnProperty(c) && (n != null || u != null))
                    switch (c) {
                    case "value":
                        z = n;
                        break;
                    case "defaultValue":
                        A = n;
                        break;
                    case "children":
                        break;
                    case "dangerouslySetInnerHTML":
                        if (n != null)
                            throw Error(f(91));
                        break;
                    default:
                        n !== u && yt(t, e, c, n, a, u)
                    }
            pf(t, z, A);
            return;
        case "option":
            for (var G in l)
                if (z = l[G],
                l.hasOwnProperty(G) && z != null && !a.hasOwnProperty(G))
                    switch (G) {
                    case "selected":
                        t.selected = !1;
                        break;
                    default:
                        yt(t, e, G, null, a, z)
                    }
            for (h in a)
                if (z = a[h],
                A = l[h],
                a.hasOwnProperty(h) && z !== A && (z != null || A != null))
                    switch (h) {
                    case "selected":
                        t.selected = z && typeof z != "function" && typeof z != "symbol";
                        break;
                    default:
                        yt(t, e, h, z, a, A)
                    }
            return;
        case "img":
        case "link":
        case "area":
        case "base":
        case "br":
        case "col":
        case "embed":
        case "hr":
        case "keygen":
        case "meta":
        case "param":
        case "source":
        case "track":
        case "wbr":
        case "menuitem":
            for (var k in l)
                z = l[k],
                l.hasOwnProperty(k) && z != null && !a.hasOwnProperty(k) && yt(t, e, k, null, a, z);
            for (E in a)
                if (z = a[E],
                A = l[E],
                a.hasOwnProperty(E) && z !== A && (z != null || A != null))
                    switch (E) {
                    case "children":
                    case "dangerouslySetInnerHTML":
                        if (z != null)
                            throw Error(f(137, e));
                        break;
                    default:
                        yt(t, e, E, z, a, A)
                    }
            return;
        default:
            if (Oi(e)) {
                for (var vt in l)
                    z = l[vt],
                    l.hasOwnProperty(vt) && z !== void 0 && !a.hasOwnProperty(vt) && xs(t, e, vt, void 0, a, z);
                for (O in a)
                    z = a[O],
                    A = l[O],
                    !a.hasOwnProperty(O) || z === A || z === void 0 && A === void 0 || xs(t, e, O, z, a, A);
                return
            }
        }
        for (var b in l)
            z = l[b],
            l.hasOwnProperty(b) && z != null && !a.hasOwnProperty(b) && yt(t, e, b, null, a, z);
        for (C in a)
            z = a[C],
            A = l[C],
            !a.hasOwnProperty(C) || z === A || z == null && A == null || yt(t, e, C, z, a, A)
    }
    function Ed(t) {
        switch (t) {
        case "css":
        case "script":
        case "font":
        case "img":
        case "image":
        case "input":
        case "link":
            return !0;
        default:
            return !1
        }
    }
    function H0() {
        if (typeof performance.getEntriesByType == "function") {
            for (var t = 0, e = 0, l = performance.getEntriesByType("resource"), a = 0; a < l.length; a++) {
                var n = l[a]
                  , u = n.transferSize
                  , c = n.initiatorType
                  , r = n.duration;
                if (u && r && Ed(c)) {
                    for (c = 0,
                    r = n.responseEnd,
                    a += 1; a < l.length; a++) {
                        var h = l[a]
                          , E = h.startTime;
                        if (E > r)
                            break;
                        var O = h.transferSize
                          , C = h.initiatorType;
                        O && Ed(C) && (h = h.responseEnd,
                        c += O * (h < r ? 1 : (r - E) / (h - E)))
                    }
                    if (--a,
                    e += 8 * (u + c) / (n.duration / 1e3),
                    t++,
                    10 < t)
                        break
                }
            }
            if (0 < t)
                return e / t / 1e6
        }
        return navigator.connection && (t = navigator.connection.downlink,
        typeof t == "number") ? t : 5
    }
    var ys = null
      , vs = null;
    function ku(t) {
        return t.nodeType === 9 ? t : t.ownerDocument
    }
    function zd(t) {
        switch (t) {
        case "http://www.w3.org/2000/svg":
            return 1;
        case "http://www.w3.org/1998/Math/MathML":
            return 2;
        default:
            return 0
        }
    }
    function Td(t, e) {
        if (t === 0)
            switch (e) {
            case "svg":
                return 1;
            case "math":
                return 2;
            default:
                return 0
            }
        return t === 1 && e === "foreignObject" ? 0 : t
    }
    function ps(t, e) {
        return t === "textarea" || t === "noscript" || typeof e.children == "string" || typeof e.children == "number" || typeof e.children == "bigint" || typeof e.dangerouslySetInnerHTML == "object" && e.dangerouslySetInnerHTML !== null && e.dangerouslySetInnerHTML.__html != null
    }
    var bs = null;
    function q0() {
        var t = window.event;
        return t && t.type === "popstate" ? t === bs ? !1 : (bs = t,
        !0) : (bs = null,
        !1)
    }
    var Ad = typeof setTimeout == "function" ? setTimeout : void 0
      , B0 = typeof clearTimeout == "function" ? clearTimeout : void 0
      , _d = typeof Promise == "function" ? Promise : void 0
      , Y0 = typeof queueMicrotask == "function" ? queueMicrotask : typeof _d < "u" ? function(t) {
        return _d.resolve(null).then(t).catch(L0)
    }
    : Ad;
    function L0(t) {
        setTimeout(function() {
            throw t
        })
    }
    function _l(t) {
        return t === "head"
    }
    function Md(t, e) {
        var l = e
          , a = 0;
        do {
            var n = l.nextSibling;
            if (t.removeChild(l),
            n && n.nodeType === 8)
                if (l = n.data,
                l === "/$" || l === "/&") {
                    if (a === 0) {
                        t.removeChild(n),
                        Ya(e);
                        return
                    }
                    a--
                } else if (l === "$" || l === "$?" || l === "$~" || l === "$!" || l === "&")
                    a++;
                else if (l === "html")
                    On(t.ownerDocument.documentElement);
                else if (l === "head") {
                    l = t.ownerDocument.head,
                    On(l);
                    for (var u = l.firstChild; u; ) {
                        var c = u.nextSibling
                          , r = u.nodeName;
                        u[Ja] || r === "SCRIPT" || r === "STYLE" || r === "LINK" && u.rel.toLowerCase() === "stylesheet" || l.removeChild(u),
                        u = c
                    }
                } else
                    l === "body" && On(t.ownerDocument.body);
            l = n
        } while (l);
        Ya(e)
    }
    function Od(t, e) {
        var l = t;
        t = 0;
        do {
            var a = l.nextSibling;
            if (l.nodeType === 1 ? e ? (l._stashedDisplay = l.style.display,
            l.style.display = "none") : (l.style.display = l._stashedDisplay || "",
            l.getAttribute("style") === "" && l.removeAttribute("style")) : l.nodeType === 3 && (e ? (l._stashedText = l.nodeValue,
            l.nodeValue = "") : l.nodeValue = l._stashedText || ""),
            a && a.nodeType === 8)
                if (l = a.data,
                l === "/$") {
                    if (t === 0)
                        break;
                    t--
                } else
                    l !== "$" && l !== "$?" && l !== "$~" && l !== "$!" || t++;
            l = a
        } while (l)
    }
    function Ss(t) {
        var e = t.firstChild;
        for (e && e.nodeType === 10 && (e = e.nextSibling); e; ) {
            var l = e;
            switch (e = e.nextSibling,
            l.nodeName) {
            case "HTML":
            case "HEAD":
            case "BODY":
                Ss(l),
                Ti(l);
                continue;
            case "SCRIPT":
            case "STYLE":
                continue;
            case "LINK":
                if (l.rel.toLowerCase() === "stylesheet")
                    continue
            }
            t.removeChild(l)
        }
    }
    function G0(t, e, l, a) {
        for (; t.nodeType === 1; ) {
            var n = l;
            if (t.nodeName.toLowerCase() !== e.toLowerCase()) {
                if (!a && (t.nodeName !== "INPUT" || t.type !== "hidden"))
                    break
            } else if (a) {
                if (!t[Ja])
                    switch (e) {
                    case "meta":
                        if (!t.hasAttribute("itemprop"))
                            break;
                        return t;
                    case "link":
                        if (u = t.getAttribute("rel"),
                        u === "stylesheet" && t.hasAttribute("data-precedence"))
                            break;
                        if (u !== n.rel || t.getAttribute("href") !== (n.href == null || n.href === "" ? null : n.href) || t.getAttribute("crossorigin") !== (n.crossOrigin == null ? null : n.crossOrigin) || t.getAttribute("title") !== (n.title == null ? null : n.title))
                            break;
                        return t;
                    case "style":
                        if (t.hasAttribute("data-precedence"))
                            break;
                        return t;
                    case "script":
                        if (u = t.getAttribute("src"),
                        (u !== (n.src == null ? null : n.src) || t.getAttribute("type") !== (n.type == null ? null : n.type) || t.getAttribute("crossorigin") !== (n.crossOrigin == null ? null : n.crossOrigin)) && u && t.hasAttribute("async") && !t.hasAttribute("itemprop"))
                            break;
                        return t;
                    default:
                        return t
                    }
            } else if (e === "input" && t.type === "hidden") {
                var u = n.name == null ? null : "" + n.name;
                if (n.type === "hidden" && t.getAttribute("name") === u)
                    return t
            } else
                return t;
            if (t = Te(t.nextSibling),
            t === null)
                break
        }
        return null
    }
    function X0(t, e, l) {
        if (e === "")
            return null;
        for (; t.nodeType !== 3; )
            if ((t.nodeType !== 1 || t.nodeName !== "INPUT" || t.type !== "hidden") && !l || (t = Te(t.nextSibling),
            t === null))
                return null;
        return t
    }
    function wd(t, e) {
        for (; t.nodeType !== 8; )
            if ((t.nodeType !== 1 || t.nodeName !== "INPUT" || t.type !== "hidden") && !e || (t = Te(t.nextSibling),
            t === null))
                return null;
        return t
    }
    function Ns(t) {
        return t.data === "$?" || t.data === "$~"
    }
    function js(t) {
        return t.data === "$!" || t.data === "$?" && t.ownerDocument.readyState !== "loading"
    }
    function Q0(t, e) {
        var l = t.ownerDocument;
        if (t.data === "$~")
            t._reactRetry = e;
        else if (t.data !== "$?" || l.readyState !== "loading")
            e();
        else {
            var a = function() {
                e(),
                l.removeEventListener("DOMContentLoaded", a)
            };
            l.addEventListener("DOMContentLoaded", a),
            t._reactRetry = a
        }
    }
    function Te(t) {
        for (; t != null; t = t.nextSibling) {
            var e = t.nodeType;
            if (e === 1 || e === 3)
                break;
            if (e === 8) {
                if (e = t.data,
                e === "$" || e === "$!" || e === "$?" || e === "$~" || e === "&" || e === "F!" || e === "F")
                    break;
                if (e === "/$" || e === "/&")
                    return null
            }
        }
        return t
    }
    var Es = null;
    function Dd(t) {
        t = t.nextSibling;
        for (var e = 0; t; ) {
            if (t.nodeType === 8) {
                var l = t.data;
                if (l === "/$" || l === "/&") {
                    if (e === 0)
                        return Te(t.nextSibling);
                    e--
                } else
                    l !== "$" && l !== "$!" && l !== "$?" && l !== "$~" && l !== "&" || e++
            }
            t = t.nextSibling
        }
        return null
    }
    function Cd(t) {
        t = t.previousSibling;
        for (var e = 0; t; ) {
            if (t.nodeType === 8) {
                var l = t.data;
                if (l === "$" || l === "$!" || l === "$?" || l === "$~" || l === "&") {
                    if (e === 0)
                        return t;
                    e--
                } else
                    l !== "/$" && l !== "/&" || e++
            }
            t = t.previousSibling
        }
        return null
    }
    function Rd(t, e, l) {
        switch (e = ku(l),
        t) {
        case "html":
            if (t = e.documentElement,
            !t)
                throw Error(f(452));
            return t;
        case "head":
            if (t = e.head,
            !t)
                throw Error(f(453));
            return t;
        case "body":
            if (t = e.body,
            !t)
                throw Error(f(454));
            return t;
        default:
            throw Error(f(451))
        }
    }
    function On(t) {
        for (var e = t.attributes; e.length; )
            t.removeAttributeNode(e[0]);
        Ti(t)
    }
    var Ae = new Map
      , Ud = new Set;
    function $u(t) {
        return typeof t.getRootNode == "function" ? t.getRootNode() : t.nodeType === 9 ? t : t.ownerDocument
    }
    var ul = q.d;
    q.d = {
        f: Z0,
        r: V0,
        D: K0,
        C: J0,
        L: k0,
        m: $0,
        X: F0,
        S: W0,
        M: I0
    };
    function Z0() {
        var t = ul.f()
          , e = Lu();
        return t || e
    }
    function V0(t) {
        var e = na(t);
        e !== null && e.tag === 5 && e.type === "form" ? Fr(e) : ul.r(t)
    }
    var Ha = typeof document > "u" ? null : document;
    function Hd(t, e, l) {
        var a = Ha;
        if (a && typeof e == "string" && e) {
            var n = pe(e);
            n = 'link[rel="' + t + '"][href="' + n + '"]',
            typeof l == "string" && (n += '[crossorigin="' + l + '"]'),
            Ud.has(n) || (Ud.add(n),
            t = {
                rel: t,
                crossOrigin: l,
                href: e
            },
            a.querySelector(n) === null && (e = a.createElement("link"),
            Jt(e, "link", t),
            Gt(e),
            a.head.appendChild(e)))
        }
    }
    function K0(t) {
        ul.D(t),
        Hd("dns-prefetch", t, null)
    }
    function J0(t, e) {
        ul.C(t, e),
        Hd("preconnect", t, e)
    }
    function k0(t, e, l) {
        ul.L(t, e, l);
        var a = Ha;
        if (a && t && e) {
            var n = 'link[rel="preload"][as="' + pe(e) + '"]';
            e === "image" && l && l.imageSrcSet ? (n += '[imagesrcset="' + pe(l.imageSrcSet) + '"]',
            typeof l.imageSizes == "string" && (n += '[imagesizes="' + pe(l.imageSizes) + '"]')) : n += '[href="' + pe(t) + '"]';
            var u = n;
            switch (e) {
            case "style":
                u = qa(t);
                break;
            case "script":
                u = Ba(t)
            }
            Ae.has(u) || (t = _({
                rel: "preload",
                href: e === "image" && l && l.imageSrcSet ? void 0 : t,
                as: e
            }, l),
            Ae.set(u, t),
            a.querySelector(n) !== null || e === "style" && a.querySelector(wn(u)) || e === "script" && a.querySelector(Dn(u)) || (e = a.createElement("link"),
            Jt(e, "link", t),
            Gt(e),
            a.head.appendChild(e)))
        }
    }
    function $0(t, e) {
        ul.m(t, e);
        var l = Ha;
        if (l && t) {
            var a = e && typeof e.as == "string" ? e.as : "script"
              , n = 'link[rel="modulepreload"][as="' + pe(a) + '"][href="' + pe(t) + '"]'
              , u = n;
            switch (a) {
            case "audioworklet":
            case "paintworklet":
            case "serviceworker":
            case "sharedworker":
            case "worker":
            case "script":
                u = Ba(t)
            }
            if (!Ae.has(u) && (t = _({
                rel: "modulepreload",
                href: t
            }, e),
            Ae.set(u, t),
            l.querySelector(n) === null)) {
                switch (a) {
                case "audioworklet":
                case "paintworklet":
                case "serviceworker":
                case "sharedworker":
                case "worker":
                case "script":
                    if (l.querySelector(Dn(u)))
                        return
                }
                a = l.createElement("link"),
                Jt(a, "link", t),
                Gt(a),
                l.head.appendChild(a)
            }
        }
    }
    function W0(t, e, l) {
        ul.S(t, e, l);
        var a = Ha;
        if (a && t) {
            var n = ua(a).hoistableStyles
              , u = qa(t);
            e = e || "default";
            var c = n.get(u);
            if (!c) {
                var r = {
                    loading: 0,
                    preload: null
                };
                if (c = a.querySelector(wn(u)))
                    r.loading = 5;
                else {
                    t = _({
                        rel: "stylesheet",
                        href: t,
                        "data-precedence": e
                    }, l),
                    (l = Ae.get(u)) && zs(t, l);
                    var h = c = a.createElement("link");
                    Gt(h),
                    Jt(h, "link", t),
                    h._p = new Promise(function(E, O) {
                        h.onload = E,
                        h.onerror = O
                    }
                    ),
                    h.addEventListener("load", function() {
                        r.loading |= 1
                    }),
                    h.addEventListener("error", function() {
                        r.loading |= 2
                    }),
                    r.loading |= 4,
                    Wu(c, e, a)
                }
                c = {
                    type: "stylesheet",
                    instance: c,
                    count: 1,
                    state: r
                },
                n.set(u, c)
            }
        }
    }
    function F0(t, e) {
        ul.X(t, e);
        var l = Ha;
        if (l && t) {
            var a = ua(l).hoistableScripts
              , n = Ba(t)
              , u = a.get(n);
            u || (u = l.querySelector(Dn(n)),
            u || (t = _({
                src: t,
                async: !0
            }, e),
            (e = Ae.get(n)) && Ts(t, e),
            u = l.createElement("script"),
            Gt(u),
            Jt(u, "link", t),
            l.head.appendChild(u)),
            u = {
                type: "script",
                instance: u,
                count: 1,
                state: null
            },
            a.set(n, u))
        }
    }
    function I0(t, e) {
        ul.M(t, e);
        var l = Ha;
        if (l && t) {
            var a = ua(l).hoistableScripts
              , n = Ba(t)
              , u = a.get(n);
            u || (u = l.querySelector(Dn(n)),
            u || (t = _({
                src: t,
                async: !0,
                type: "module"
            }, e),
            (e = Ae.get(n)) && Ts(t, e),
            u = l.createElement("script"),
            Gt(u),
            Jt(u, "link", t),
            l.head.appendChild(u)),
            u = {
                type: "script",
                instance: u,
                count: 1,
                state: null
            },
            a.set(n, u))
        }
    }
    function qd(t, e, l, a) {
        var n = (n = lt.current) ? $u(n) : null;
        if (!n)
            throw Error(f(446));
        switch (t) {
        case "meta":
        case "title":
            return null;
        case "style":
            return typeof l.precedence == "string" && typeof l.href == "string" ? (e = qa(l.href),
            l = ua(n).hoistableStyles,
            a = l.get(e),
            a || (a = {
                type: "style",
                instance: null,
                count: 0,
                state: null
            },
            l.set(e, a)),
            a) : {
                type: "void",
                instance: null,
                count: 0,
                state: null
            };
        case "link":
            if (l.rel === "stylesheet" && typeof l.href == "string" && typeof l.precedence == "string") {
                t = qa(l.href);
                var u = ua(n).hoistableStyles
                  , c = u.get(t);
                if (c || (n = n.ownerDocument || n,
                c = {
                    type: "stylesheet",
                    instance: null,
                    count: 0,
                    state: {
                        loading: 0,
                        preload: null
                    }
                },
                u.set(t, c),
                (u = n.querySelector(wn(t))) && !u._p && (c.instance = u,
                c.state.loading = 5),
                Ae.has(t) || (l = {
                    rel: "preload",
                    as: "style",
                    href: l.href,
                    crossOrigin: l.crossOrigin,
                    integrity: l.integrity,
                    media: l.media,
                    hrefLang: l.hrefLang,
                    referrerPolicy: l.referrerPolicy
                },
                Ae.set(t, l),
                u || P0(n, t, l, c.state))),
                e && a === null)
                    throw Error(f(528, ""));
                return c
            }
            if (e && a !== null)
                throw Error(f(529, ""));
            return null;
        case "script":
            return e = l.async,
            l = l.src,
            typeof l == "string" && e && typeof e != "function" && typeof e != "symbol" ? (e = Ba(l),
            l = ua(n).hoistableScripts,
            a = l.get(e),
            a || (a = {
                type: "script",
                instance: null,
                count: 0,
                state: null
            },
            l.set(e, a)),
            a) : {
                type: "void",
                instance: null,
                count: 0,
                state: null
            };
        default:
            throw Error(f(444, t))
        }
    }
    function qa(t) {
        return 'href="' + pe(t) + '"'
    }
    function wn(t) {
        return 'link[rel="stylesheet"][' + t + "]"
    }
    function Bd(t) {
        return _({}, t, {
            "data-precedence": t.precedence,
            precedence: null
        })
    }
    function P0(t, e, l, a) {
        t.querySelector('link[rel="preload"][as="style"][' + e + "]") ? a.loading = 1 : (e = t.createElement("link"),
        a.preload = e,
        e.addEventListener("load", function() {
            return a.loading |= 1
        }),
        e.addEventListener("error", function() {
            return a.loading |= 2
        }),
        Jt(e, "link", l),
        Gt(e),
        t.head.appendChild(e))
    }
    function Ba(t) {
        return '[src="' + pe(t) + '"]'
    }
    function Dn(t) {
        return "script[async]" + t
    }
    function Yd(t, e, l) {
        if (e.count++,
        e.instance === null)
            switch (e.type) {
            case "style":
                var a = t.querySelector('style[data-href~="' + pe(l.href) + '"]');
                if (a)
                    return e.instance = a,
                    Gt(a),
                    a;
                var n = _({}, l, {
                    "data-href": l.href,
                    "data-precedence": l.precedence,
                    href: null,
                    precedence: null
                });
                return a = (t.ownerDocument || t).createElement("style"),
                Gt(a),
                Jt(a, "style", n),
                Wu(a, l.precedence, t),
                e.instance = a;
            case "stylesheet":
                n = qa(l.href);
                var u = t.querySelector(wn(n));
                if (u)
                    return e.state.loading |= 4,
                    e.instance = u,
                    Gt(u),
                    u;
                a = Bd(l),
                (n = Ae.get(n)) && zs(a, n),
                u = (t.ownerDocument || t).createElement("link"),
                Gt(u);
                var c = u;
                return c._p = new Promise(function(r, h) {
                    c.onload = r,
                    c.onerror = h
                }
                ),
                Jt(u, "link", a),
                e.state.loading |= 4,
                Wu(u, l.precedence, t),
                e.instance = u;
            case "script":
                return u = Ba(l.src),
                (n = t.querySelector(Dn(u))) ? (e.instance = n,
                Gt(n),
                n) : (a = l,
                (n = Ae.get(u)) && (a = _({}, l),
                Ts(a, n)),
                t = t.ownerDocument || t,
                n = t.createElement("script"),
                Gt(n),
                Jt(n, "link", a),
                t.head.appendChild(n),
                e.instance = n);
            case "void":
                return null;
            default:
                throw Error(f(443, e.type))
            }
        else
            e.type === "stylesheet" && (e.state.loading & 4) === 0 && (a = e.instance,
            e.state.loading |= 4,
            Wu(a, l.precedence, t));
        return e.instance
    }
    function Wu(t, e, l) {
        for (var a = l.querySelectorAll('link[rel="stylesheet"][data-precedence],style[data-precedence]'), n = a.length ? a[a.length - 1] : null, u = n, c = 0; c < a.length; c++) {
            var r = a[c];
            if (r.dataset.precedence === e)
                u = r;
            else if (u !== n)
                break
        }
        u ? u.parentNode.insertBefore(t, u.nextSibling) : (e = l.nodeType === 9 ? l.head : l,
        e.insertBefore(t, e.firstChild))
    }
    function zs(t, e) {
        t.crossOrigin == null && (t.crossOrigin = e.crossOrigin),
        t.referrerPolicy == null && (t.referrerPolicy = e.referrerPolicy),
        t.title == null && (t.title = e.title)
    }
    function Ts(t, e) {
        t.crossOrigin == null && (t.crossOrigin = e.crossOrigin),
        t.referrerPolicy == null && (t.referrerPolicy = e.referrerPolicy),
        t.integrity == null && (t.integrity = e.integrity)
    }
    var Fu = null;
    function Ld(t, e, l) {
        if (Fu === null) {
            var a = new Map
              , n = Fu = new Map;
            n.set(l, a)
        } else
            n = Fu,
            a = n.get(l),
            a || (a = new Map,
            n.set(l, a));
        if (a.has(t))
            return a;
        for (a.set(t, null),
        l = l.getElementsByTagName(t),
        n = 0; n < l.length; n++) {
            var u = l[n];
            if (!(u[Ja] || u[Qt] || t === "link" && u.getAttribute("rel") === "stylesheet") && u.namespaceURI !== "http://www.w3.org/2000/svg") {
                var c = u.getAttribute(e) || "";
                c = t + c;
                var r = a.get(c);
                r ? r.push(u) : a.set(c, [u])
            }
        }
        return a
    }
    function Gd(t, e, l) {
        t = t.ownerDocument || t,
        t.head.insertBefore(l, e === "title" ? t.querySelector("head > title") : null)
    }
    function tg(t, e, l) {
        if (l === 1 || e.itemProp != null)
            return !1;
        switch (t) {
        case "meta":
        case "title":
            return !0;
        case "style":
            if (typeof e.precedence != "string" || typeof e.href != "string" || e.href === "")
                break;
            return !0;
        case "link":
            if (typeof e.rel != "string" || typeof e.href != "string" || e.href === "" || e.onLoad || e.onError)
                break;
            switch (e.rel) {
            case "stylesheet":
                return t = e.disabled,
                typeof e.precedence == "string" && t == null;
            default:
                return !0
            }
        case "script":
            if (e.async && typeof e.async != "function" && typeof e.async != "symbol" && !e.onLoad && !e.onError && e.src && typeof e.src == "string")
                return !0
        }
        return !1
    }
    function Xd(t) {
        return !(t.type === "stylesheet" && (t.state.loading & 3) === 0)
    }
    function eg(t, e, l, a) {
        if (l.type === "stylesheet" && (typeof a.media != "string" || matchMedia(a.media).matches !== !1) && (l.state.loading & 4) === 0) {
            if (l.instance === null) {
                var n = qa(a.href)
                  , u = e.querySelector(wn(n));
                if (u) {
                    e = u._p,
                    e !== null && typeof e == "object" && typeof e.then == "function" && (t.count++,
                    t = Iu.bind(t),
                    e.then(t, t)),
                    l.state.loading |= 4,
                    l.instance = u,
                    Gt(u);
                    return
                }
                u = e.ownerDocument || e,
                a = Bd(a),
                (n = Ae.get(n)) && zs(a, n),
                u = u.createElement("link"),
                Gt(u);
                var c = u;
                c._p = new Promise(function(r, h) {
                    c.onload = r,
                    c.onerror = h
                }
                ),
                Jt(u, "link", a),
                l.instance = u
            }
            t.stylesheets === null && (t.stylesheets = new Map),
            t.stylesheets.set(l, e),
            (e = l.state.preload) && (l.state.loading & 3) === 0 && (t.count++,
            l = Iu.bind(t),
            e.addEventListener("load", l),
            e.addEventListener("error", l))
        }
    }
    var As = 0;
    function lg(t, e) {
        return t.stylesheets && t.count === 0 && ti(t, t.stylesheets),
        0 < t.count || 0 < t.imgCount ? function(l) {
            var a = setTimeout(function() {
                if (t.stylesheets && ti(t, t.stylesheets),
                t.unsuspend) {
                    var u = t.unsuspend;
                    t.unsuspend = null,
                    u()
                }
            }, 6e4 + e);
            0 < t.imgBytes && As === 0 && (As = 62500 * H0());
            var n = setTimeout(function() {
                if (t.waitingForImages = !1,
                t.count === 0 && (t.stylesheets && ti(t, t.stylesheets),
                t.unsuspend)) {
                    var u = t.unsuspend;
                    t.unsuspend = null,
                    u()
                }
            }, (t.imgBytes > As ? 50 : 800) + e);
            return t.unsuspend = l,
            function() {
                t.unsuspend = null,
                clearTimeout(a),
                clearTimeout(n)
            }
        }
        : null
    }
    function Iu() {
        if (this.count--,
        this.count === 0 && (this.imgCount === 0 || !this.waitingForImages)) {
            if (this.stylesheets)
                ti(this, this.stylesheets);
            else if (this.unsuspend) {
                var t = this.unsuspend;
                this.unsuspend = null,
                t()
            }
        }
    }
    var Pu = null;
    function ti(t, e) {
        t.stylesheets = null,
        t.unsuspend !== null && (t.count++,
        Pu = new Map,
        e.forEach(ag, t),
        Pu = null,
        Iu.call(t))
    }
    function ag(t, e) {
        if (!(e.state.loading & 4)) {
            var l = Pu.get(t);
            if (l)
                var a = l.get(null);
            else {
                l = new Map,
                Pu.set(t, l);
                for (var n = t.querySelectorAll("link[data-precedence],style[data-precedence]"), u = 0; u < n.length; u++) {
                    var c = n[u];
                    (c.nodeName === "LINK" || c.getAttribute("media") !== "not all") && (l.set(c.dataset.precedence, c),
                    a = c)
                }
                a && l.set(null, a)
            }
            n = e.instance,
            c = n.getAttribute("data-precedence"),
            u = l.get(c) || a,
            u === a && l.set(null, n),
            l.set(c, n),
            this.count++,
            a = Iu.bind(this),
            n.addEventListener("load", a),
            n.addEventListener("error", a),
            u ? u.parentNode.insertBefore(n, u.nextSibling) : (t = t.nodeType === 9 ? t.head : t,
            t.insertBefore(n, t.firstChild)),
            e.state.loading |= 4
        }
    }
    var Cn = {
        $$typeof: Y,
        Provider: null,
        Consumer: null,
        _currentValue: $,
        _currentValue2: $,
        _threadCount: 0
    };
    function ng(t, e, l, a, n, u, c, r, h) {
        this.tag = 1,
        this.containerInfo = t,
        this.pingCache = this.current = this.pendingChildren = null,
        this.timeoutHandle = -1,
        this.callbackNode = this.next = this.pendingContext = this.context = this.cancelPendingCommit = null,
        this.callbackPriority = 0,
        this.expirationTimes = Ni(-1),
        this.entangledLanes = this.shellSuspendCounter = this.errorRecoveryDisabledLanes = this.expiredLanes = this.warmLanes = this.pingedLanes = this.suspendedLanes = this.pendingLanes = 0,
        this.entanglements = Ni(0),
        this.hiddenUpdates = Ni(null),
        this.identifierPrefix = a,
        this.onUncaughtError = n,
        this.onCaughtError = u,
        this.onRecoverableError = c,
        this.pooledCache = null,
        this.pooledCacheLanes = 0,
        this.formState = h,
        this.incompleteTransitions = new Map
    }
    function Qd(t, e, l, a, n, u, c, r, h, E, O, C) {
        return t = new ng(t,e,l,c,h,E,O,C,r),
        e = 1,
        u === !0 && (e |= 24),
        u = de(3, null, null, e),
        t.current = u,
        u.stateNode = t,
        e = ic(),
        e.refCount++,
        t.pooledCache = e,
        e.refCount++,
        u.memoizedState = {
            element: a,
            isDehydrated: l,
            cache: e
        },
        rc(u),
        t
    }
    function Zd(t) {
        return t ? (t = ga,
        t) : ga
    }
    function Vd(t, e, l, a, n, u) {
        n = Zd(n),
        a.context === null ? a.context = n : a.pendingContext = n,
        a = yl(e),
        a.payload = {
            element: l
        },
        u = u === void 0 ? null : u,
        u !== null && (a.callback = u),
        l = vl(t, a, e),
        l !== null && (ne(l, t, e),
        on(l, t, e))
    }
    function Kd(t, e) {
        if (t = t.memoizedState,
        t !== null && t.dehydrated !== null) {
            var l = t.retryLane;
            t.retryLane = l !== 0 && l < e ? l : e
        }
    }
    function _s(t, e) {
        Kd(t, e),
        (t = t.alternate) && Kd(t, e)
    }
    function Jd(t) {
        if (t.tag === 13 || t.tag === 31) {
            var e = Gl(t, 67108864);
            e !== null && ne(e, t, 67108864),
            _s(t, 67108864)
        }
    }
    function kd(t) {
        if (t.tag === 13 || t.tag === 31) {
            var e = ye();
            e = ji(e);
            var l = Gl(t, e);
            l !== null && ne(l, t, e),
            _s(t, e)
        }
    }
    var ei = !0;
    function ug(t, e, l, a) {
        var n = w.T;
        w.T = null;
        var u = q.p;
        try {
            q.p = 2,
            Ms(t, e, l, a)
        } finally {
            q.p = u,
            w.T = n
        }
    }
    function ig(t, e, l, a) {
        var n = w.T;
        w.T = null;
        var u = q.p;
        try {
            q.p = 8,
            Ms(t, e, l, a)
        } finally {
            q.p = u,
            w.T = n
        }
    }
    function Ms(t, e, l, a) {
        if (ei) {
            var n = Os(a);
            if (n === null)
                gs(t, e, a, li, l),
                Wd(t, a);
            else if (sg(n, t, e, l, a))
                a.stopPropagation();
            else if (Wd(t, a),
            e & 4 && -1 < cg.indexOf(t)) {
                for (; n !== null; ) {
                    var u = na(n);
                    if (u !== null)
                        switch (u.tag) {
                        case 3:
                            if (u = u.stateNode,
                            u.current.memoizedState.isDehydrated) {
                                var c = Hl(u.pendingLanes);
                                if (c !== 0) {
                                    var r = u;
                                    for (r.pendingLanes |= 2,
                                    r.entangledLanes |= 2; c; ) {
                                        var h = 1 << 31 - re(c);
                                        r.entanglements[1] |= h,
                                        c &= ~h
                                    }
                                    qe(u),
                                    (rt & 6) === 0 && (Bu = se() + 500,
                                    An(0))
                                }
                            }
                            break;
                        case 31:
                        case 13:
                            r = Gl(u, 2),
                            r !== null && ne(r, u, 2),
                            Lu(),
                            _s(u, 2)
                        }
                    if (u = Os(a),
                    u === null && gs(t, e, a, li, l),
                    u === n)
                        break;
                    n = u
                }
                n !== null && a.stopPropagation()
            } else
                gs(t, e, a, null, l)
        }
    }
    function Os(t) {
        return t = Di(t),
        ws(t)
    }
    var li = null;
    function ws(t) {
        if (li = null,
        t = aa(t),
        t !== null) {
            var e = g(t);
            if (e === null)
                t = null;
            else {
                var l = e.tag;
                if (l === 13) {
                    if (t = p(e),
                    t !== null)
                        return t;
                    t = null
                } else if (l === 31) {
                    if (t = T(e),
                    t !== null)
                        return t;
                    t = null
                } else if (l === 3) {
                    if (e.stateNode.current.memoizedState.isDehydrated)
                        return e.tag === 3 ? e.stateNode.containerInfo : null;
                    t = null
                } else
                    e !== t && (t = null)
            }
        }
        return li = t,
        null
    }
    function $d(t) {
        switch (t) {
        case "beforetoggle":
        case "cancel":
        case "click":
        case "close":
        case "contextmenu":
        case "copy":
        case "cut":
        case "auxclick":
        case "dblclick":
        case "dragend":
        case "dragstart":
        case "drop":
        case "focusin":
        case "focusout":
        case "input":
        case "invalid":
        case "keydown":
        case "keypress":
        case "keyup":
        case "mousedown":
        case "mouseup":
        case "paste":
        case "pause":
        case "play":
        case "pointercancel":
        case "pointerdown":
        case "pointerup":
        case "ratechange":
        case "reset":
        case "resize":
        case "seeked":
        case "submit":
        case "toggle":
        case "touchcancel":
        case "touchend":
        case "touchstart":
        case "volumechange":
        case "change":
        case "selectionchange":
        case "textInput":
        case "compositionstart":
        case "compositionend":
        case "compositionupdate":
        case "beforeblur":
        case "afterblur":
        case "beforeinput":
        case "blur":
        case "fullscreenchange":
        case "focus":
        case "hashchange":
        case "popstate":
        case "select":
        case "selectstart":
            return 2;
        case "drag":
        case "dragenter":
        case "dragexit":
        case "dragleave":
        case "dragover":
        case "mousemove":
        case "mouseout":
        case "mouseover":
        case "pointermove":
        case "pointerout":
        case "pointerover":
        case "scroll":
        case "touchmove":
        case "wheel":
        case "mouseenter":
        case "mouseleave":
        case "pointerenter":
        case "pointerleave":
            return 8;
        case "message":
            switch (Km()) {
            case ef:
                return 2;
            case lf:
                return 8;
            case Vn:
            case Jm:
                return 32;
            case af:
                return 268435456;
            default:
                return 32
            }
        default:
            return 32
        }
    }
    var Ds = !1
      , Ml = null
      , Ol = null
      , wl = null
      , Rn = new Map
      , Un = new Map
      , Dl = []
      , cg = "mousedown mouseup touchcancel touchend touchstart auxclick dblclick pointercancel pointerdown pointerup dragend dragstart drop compositionend compositionstart keydown keypress keyup input textInput copy cut paste click change contextmenu reset".split(" ");
    function Wd(t, e) {
        switch (t) {
        case "focusin":
        case "focusout":
            Ml = null;
            break;
        case "dragenter":
        case "dragleave":
            Ol = null;
            break;
        case "mouseover":
        case "mouseout":
            wl = null;
            break;
        case "pointerover":
        case "pointerout":
            Rn.delete(e.pointerId);
            break;
        case "gotpointercapture":
        case "lostpointercapture":
            Un.delete(e.pointerId)
        }
    }
    function Hn(t, e, l, a, n, u) {
        return t === null || t.nativeEvent !== u ? (t = {
            blockedOn: e,
            domEventName: l,
            eventSystemFlags: a,
            nativeEvent: u,
            targetContainers: [n]
        },
        e !== null && (e = na(e),
        e !== null && Jd(e)),
        t) : (t.eventSystemFlags |= a,
        e = t.targetContainers,
        n !== null && e.indexOf(n) === -1 && e.push(n),
        t)
    }
    function sg(t, e, l, a, n) {
        switch (e) {
        case "focusin":
            return Ml = Hn(Ml, t, e, l, a, n),
            !0;
        case "dragenter":
            return Ol = Hn(Ol, t, e, l, a, n),
            !0;
        case "mouseover":
            return wl = Hn(wl, t, e, l, a, n),
            !0;
        case "pointerover":
            var u = n.pointerId;
            return Rn.set(u, Hn(Rn.get(u) || null, t, e, l, a, n)),
            !0;
        case "gotpointercapture":
            return u = n.pointerId,
            Un.set(u, Hn(Un.get(u) || null, t, e, l, a, n)),
            !0
        }
        return !1
    }
    function Fd(t) {
        var e = aa(t.target);
        if (e !== null) {
            var l = g(e);
            if (l !== null) {
                if (e = l.tag,
                e === 13) {
                    if (e = p(l),
                    e !== null) {
                        t.blockedOn = e,
                        rf(t.priority, function() {
                            kd(l)
                        });
                        return
                    }
                } else if (e === 31) {
                    if (e = T(l),
                    e !== null) {
                        t.blockedOn = e,
                        rf(t.priority, function() {
                            kd(l)
                        });
                        return
                    }
                } else if (e === 3 && l.stateNode.current.memoizedState.isDehydrated) {
                    t.blockedOn = l.tag === 3 ? l.stateNode.containerInfo : null;
                    return
                }
            }
        }
        t.blockedOn = null
    }
    function ai(t) {
        if (t.blockedOn !== null)
            return !1;
        for (var e = t.targetContainers; 0 < e.length; ) {
            var l = Os(t.nativeEvent);
            if (l === null) {
                l = t.nativeEvent;
                var a = new l.constructor(l.type,l);
                wi = a,
                l.target.dispatchEvent(a),
                wi = null
            } else
                return e = na(l),
                e !== null && Jd(e),
                t.blockedOn = l,
                !1;
            e.shift()
        }
        return !0
    }
    function Id(t, e, l) {
        ai(t) && l.delete(e)
    }
    function fg() {
        Ds = !1,
        Ml !== null && ai(Ml) && (Ml = null),
        Ol !== null && ai(Ol) && (Ol = null),
        wl !== null && ai(wl) && (wl = null),
        Rn.forEach(Id),
        Un.forEach(Id)
    }
    function ni(t, e) {
        t.blockedOn === e && (t.blockedOn = null,
        Ds || (Ds = !0,
        s.unstable_scheduleCallback(s.unstable_NormalPriority, fg)))
    }
    var ui = null;
    function Pd(t) {
        ui !== t && (ui = t,
        s.unstable_scheduleCallback(s.unstable_NormalPriority, function() {
            ui === t && (ui = null);
            for (var e = 0; e < t.length; e += 3) {
                var l = t[e]
                  , a = t[e + 1]
                  , n = t[e + 2];
                if (typeof a != "function") {
                    if (ws(a || l) === null)
                        continue;
                    break
                }
                var u = na(l);
                u !== null && (t.splice(e, 3),
                e -= 3,
                Oc(u, {
                    pending: !0,
                    data: n,
                    method: l.method,
                    action: a
                }, a, n))
            }
        }))
    }
    function Ya(t) {
        function e(h) {
            return ni(h, t)
        }
        Ml !== null && ni(Ml, t),
        Ol !== null && ni(Ol, t),
        wl !== null && ni(wl, t),
        Rn.forEach(e),
        Un.forEach(e);
        for (var l = 0; l < Dl.length; l++) {
            var a = Dl[l];
            a.blockedOn === t && (a.blockedOn = null)
        }
        for (; 0 < Dl.length && (l = Dl[0],
        l.blockedOn === null); )
            Fd(l),
            l.blockedOn === null && Dl.shift();
        if (l = (t.ownerDocument || t).$$reactFormReplay,
        l != null)
            for (a = 0; a < l.length; a += 3) {
                var n = l[a]
                  , u = l[a + 1]
                  , c = n[It] || null;
                if (typeof u == "function")
                    c || Pd(l);
                else if (c) {
                    var r = null;
                    if (u && u.hasAttribute("formAction")) {
                        if (n = u,
                        c = u[It] || null)
                            r = c.formAction;
                        else if (ws(n) !== null)
                            continue
                    } else
                        r = c.action;
                    typeof r == "function" ? l[a + 1] = r : (l.splice(a, 3),
                    a -= 3),
                    Pd(l)
                }
            }
    }
    function tm() {
        function t(u) {
            u.canIntercept && u.info === "react-transition" && u.intercept({
                handler: function() {
                    return new Promise(function(c) {
                        return n = c
                    }
                    )
                },
                focusReset: "manual",
                scroll: "manual"
            })
        }
        function e() {
            n !== null && (n(),
            n = null),
            a || setTimeout(l, 20)
        }
        function l() {
            if (!a && !navigation.transition) {
                var u = navigation.currentEntry;
                u && u.url != null && navigation.navigate(u.url, {
                    state: u.getState(),
                    info: "react-transition",
                    history: "replace"
                })
            }
        }
        if (typeof navigation == "object") {
            var a = !1
              , n = null;
            return navigation.addEventListener("navigate", t),
            navigation.addEventListener("navigatesuccess", e),
            navigation.addEventListener("navigateerror", e),
            setTimeout(l, 100),
            function() {
                a = !0,
                navigation.removeEventListener("navigate", t),
                navigation.removeEventListener("navigatesuccess", e),
                navigation.removeEventListener("navigateerror", e),
                n !== null && (n(),
                n = null)
            }
        }
    }
    function Cs(t) {
        this._internalRoot = t
    }
    ii.prototype.render = Cs.prototype.render = function(t) {
        var e = this._internalRoot;
        if (e === null)
            throw Error(f(409));
        var l = e.current
          , a = ye();
        Vd(l, a, t, e, null, null)
    }
    ,
    ii.prototype.unmount = Cs.prototype.unmount = function() {
        var t = this._internalRoot;
        if (t !== null) {
            this._internalRoot = null;
            var e = t.containerInfo;
            Vd(t.current, 2, null, t, null, null),
            Lu(),
            e[la] = null
        }
    }
    ;
    function ii(t) {
        this._internalRoot = t
    }
    ii.prototype.unstable_scheduleHydration = function(t) {
        if (t) {
            var e = ff();
            t = {
                blockedOn: null,
                target: t,
                priority: e
            };
            for (var l = 0; l < Dl.length && e !== 0 && e < Dl[l].priority; l++)
                ;
            Dl.splice(l, 0, t),
            l === 0 && Fd(t)
        }
    }
    ;
    var em = d.version;
    if (em !== "19.2.0")
        throw Error(f(527, em, "19.2.0"));
    q.findDOMNode = function(t) {
        var e = t._reactInternals;
        if (e === void 0)
            throw typeof t.render == "function" ? Error(f(188)) : (t = Object.keys(t).join(","),
            Error(f(268, t)));
        return t = x(e),
        t = t !== null ? N(t) : null,
        t = t === null ? null : t.stateNode,
        t
    }
    ;
    var rg = {
        bundleType: 0,
        version: "19.2.0",
        rendererPackageName: "react-dom",
        currentDispatcherRef: w,
        reconcilerVersion: "19.2.0"
    };
    if (typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ < "u") {
        var ci = __REACT_DEVTOOLS_GLOBAL_HOOK__;
        if (!ci.isDisabled && ci.supportsFiber)
            try {
                Za = ci.inject(rg),
                fe = ci
            } catch {}
    }
    return Bn.createRoot = function(t, e) {
        if (!m(t))
            throw Error(f(299));
        var l = !1
          , a = ""
          , n = co
          , u = so
          , c = fo;
        return e != null && (e.unstable_strictMode === !0 && (l = !0),
        e.identifierPrefix !== void 0 && (a = e.identifierPrefix),
        e.onUncaughtError !== void 0 && (n = e.onUncaughtError),
        e.onCaughtError !== void 0 && (u = e.onCaughtError),
        e.onRecoverableError !== void 0 && (c = e.onRecoverableError)),
        e = Qd(t, 1, !1, null, null, l, a, null, n, u, c, tm),
        t[la] = e.current,
        hs(t),
        new Cs(e)
    }
    ,
    Bn.hydrateRoot = function(t, e, l) {
        if (!m(t))
            throw Error(f(299));
        var a = !1
          , n = ""
          , u = co
          , c = so
          , r = fo
          , h = null;
        return l != null && (l.unstable_strictMode === !0 && (a = !0),
        l.identifierPrefix !== void 0 && (n = l.identifierPrefix),
        l.onUncaughtError !== void 0 && (u = l.onUncaughtError),
        l.onCaughtError !== void 0 && (c = l.onCaughtError),
        l.onRecoverableError !== void 0 && (r = l.onRecoverableError),
        l.formState !== void 0 && (h = l.formState)),
        e = Qd(t, 1, !0, e, l ?? null, a, n, h, u, c, r, tm),
        e.context = Zd(null),
        l = e.current,
        a = ye(),
        a = ji(a),
        n = yl(a),
        n.callback = null,
        vl(l, n, a),
        l = a,
        e.current.lanes = l,
        Ka(e, l),
        qe(e),
        t[la] = e.current,
        hs(t),
        new ii(e)
    }
    ,
    Bn.version = "19.2.0",
    Bn
}
var om;
function Sg() {
    if (om)
        return Hs.exports;
    om = 1;
    function s() {
        if (!(typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ > "u" || typeof __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE != "function"))
            try {
                __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE(s)
            } catch (d) {
                console.error(d)
            }
    }
    return s(),
    Hs.exports = bg(),
    Hs.exports
}
var Ng = Sg();
const jg = Sm(Ng);
/**
 * react-router v7.9.6
 *
 * Copyright (c) Remix Software Inc.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE.md file in the root directory of this source tree.
 *
 * @license MIT
 */
var dm = "popstate";
function Eg(s={}) {
    function d(m, g) {
        let {pathname: p="/", search: T="", hash: S=""} = ea(m.location.hash.substring(1));
        return !p.startsWith("/") && !p.startsWith(".") && (p = "/" + p),
        Xs("", {
            pathname: p,
            search: T,
            hash: S
        }, g.state && g.state.usr || null, g.state && g.state.key || "default")
    }
    function o(m, g) {
        let p = m.document.querySelector("base")
          , T = "";
        if (p && p.getAttribute("href")) {
            let S = m.location.href
              , x = S.indexOf("#");
            T = x === -1 ? S : S.slice(0, x)
        }
        return T + "#" + (typeof g == "string" ? g : Ln(g))
    }
    function f(m, g) {
        _e(m.pathname.charAt(0) === "/", `relative pathnames are not supported in hash history.push(${JSON.stringify(g)})`)
    }
    return Tg(d, o, f, s)
}
function Et(s, d) {
    if (s === !1 || s === null || typeof s > "u")
        throw new Error(d)
}
function _e(s, d) {
    if (!s) {
        typeof console < "u" && console.warn(d);
        try {
            throw new Error(d)
        } catch {}
    }
}
function zg() {
    return Math.random().toString(36).substring(2, 10)
}
function mm(s, d) {
    return {
        usr: s.state,
        key: s.key,
        idx: d
    }
}
function Xs(s, d, o=null, f) {
    return {
        pathname: typeof s == "string" ? s : s.pathname,
        search: "",
        hash: "",
        ...typeof d == "string" ? ea(d) : d,
        state: o,
        key: d && d.key || f || zg()
    }
}
function Ln({pathname: s="/", search: d="", hash: o=""}) {
    return d && d !== "?" && (s += d.charAt(0) === "?" ? d : "?" + d),
    o && o !== "#" && (s += o.charAt(0) === "#" ? o : "#" + o),
    s
}
function ea(s) {
    let d = {};
    if (s) {
        let o = s.indexOf("#");
        o >= 0 && (d.hash = s.substring(o),
        s = s.substring(0, o));
        let f = s.indexOf("?");
        f >= 0 && (d.search = s.substring(f),
        s = s.substring(0, f)),
        s && (d.pathname = s)
    }
    return d
}
function Tg(s, d, o, f={}) {
    let {window: m=document.defaultView, v5Compat: g=!1} = f
      , p = m.history
      , T = "POP"
      , S = null
      , x = N();
    x == null && (x = 0,
    p.replaceState({
        ...p.state,
        idx: x
    }, ""));
    function N() {
        return (p.state || {
            idx: null
        }).idx
    }
    function _() {
        T = "POP";
        let X = N()
          , Z = X == null ? null : X - x;
        x = X,
        S && S({
            action: T,
            location: J.location,
            delta: Z
        })
    }
    function H(X, Z) {
        T = "PUSH";
        let et = Xs(J.location, X, Z);
        o && o(et, X),
        x = N() + 1;
        let Y = mm(et, x)
          , dt = J.createHref(et);
        try {
            p.pushState(Y, "", dt)
        } catch (zt) {
            if (zt instanceof DOMException && zt.name === "DataCloneError")
                throw zt;
            m.location.assign(dt)
        }
        g && S && S({
            action: T,
            location: J.location,
            delta: 1
        })
    }
    function U(X, Z) {
        T = "REPLACE";
        let et = Xs(J.location, X, Z);
        o && o(et, X),
        x = N();
        let Y = mm(et, x)
          , dt = J.createHref(et);
        p.replaceState(Y, "", dt),
        g && S && S({
            action: T,
            location: J.location,
            delta: 0
        })
    }
    function L(X) {
        return Ag(X)
    }
    let J = {
        get action() {
            return T
        },
        get location() {
            return s(m, p)
        },
        listen(X) {
            if (S)
                throw new Error("A history only accepts one active listener");
            return m.addEventListener(dm, _),
            S = X,
            () => {
                m.removeEventListener(dm, _),
                S = null
            }
        },
        createHref(X) {
            return d(m, X)
        },
        createURL: L,
        encodeLocation(X) {
            let Z = L(X);
            return {
                pathname: Z.pathname,
                search: Z.search,
                hash: Z.hash
            }
        },
        push: H,
        replace: U,
        go(X) {
            return p.go(X)
        }
    };
    return J
}
function Ag(s, d=!1) {
    let o = "http://localhost";
    typeof window < "u" && (o = window.location.origin !== "null" ? window.location.origin : window.location.href),
    Et(o, "No window.location.(origin|href) available to create URL");
    let f = typeof s == "string" ? s : Ln(s);
    return f = f.replace(/ $/, "%20"),
    !d && f.startsWith("//") && (f = o + f),
    new URL(f,o)
}
function Nm(s, d, o="/") {
    return _g(s, d, o, !1)
}
function _g(s, d, o, f) {
    let m = typeof d == "string" ? ea(d) : d
      , g = cl(m.pathname || "/", o);
    if (g == null)
        return null;
    let p = jm(s);
    Mg(p);
    let T = null;
    for (let S = 0; T == null && S < p.length; ++S) {
        let x = Lg(g);
        T = Bg(p[S], x, f)
    }
    return T
}
function jm(s, d=[], o=[], f="", m=!1) {
    let g = (p, T, S=m, x) => {
        let N = {
            relativePath: x === void 0 ? p.path || "" : x,
            caseSensitive: p.caseSensitive === !0,
            childrenIndex: T,
            route: p
        };
        if (N.relativePath.startsWith("/")) {
            if (!N.relativePath.startsWith(f) && S)
                return;
            Et(N.relativePath.startsWith(f), `Absolute route path "${N.relativePath}" nested under path "${f}" is not valid. An absolute child route path must start with the combined path of all its parent routes.`),
            N.relativePath = N.relativePath.slice(f.length)
        }
        let _ = il([f, N.relativePath])
          , H = o.concat(N);
        p.children && p.children.length > 0 && (Et(p.index !== !0, `Index routes must not have child routes. Please remove all child routes from route path "${_}".`),
        jm(p.children, d, H, _, S)),
        !(p.path == null && !p.index) && d.push({
            path: _,
            score: Hg(_, p.index),
            routesMeta: H
        })
    }
    ;
    return s.forEach( (p, T) => {
        var S;
        if (p.path === "" || !((S = p.path) != null && S.includes("?")))
            g(p, T);
        else
            for (let x of Em(p.path))
                g(p, T, !0, x)
    }
    ),
    d
}
function Em(s) {
    let d = s.split("/");
    if (d.length === 0)
        return [];
    let[o,...f] = d
      , m = o.endsWith("?")
      , g = o.replace(/\?$/, "");
    if (f.length === 0)
        return m ? [g, ""] : [g];
    let p = Em(f.join("/"))
      , T = [];
    return T.push(...p.map(S => S === "" ? g : [g, S].join("/"))),
    m && T.push(...p),
    T.map(S => s.startsWith("/") && S === "" ? "/" : S)
}
function Mg(s) {
    s.sort( (d, o) => d.score !== o.score ? o.score - d.score : qg(d.routesMeta.map(f => f.childrenIndex), o.routesMeta.map(f => f.childrenIndex)))
}
var Og = /^:[\w-]+$/
  , wg = 3
  , Dg = 2
  , Cg = 1
  , Rg = 10
  , Ug = -2
  , hm = s => s === "*";
function Hg(s, d) {
    let o = s.split("/")
      , f = o.length;
    return o.some(hm) && (f += Ug),
    d && (f += Dg),
    o.filter(m => !hm(m)).reduce( (m, g) => m + (Og.test(g) ? wg : g === "" ? Cg : Rg), f)
}
function qg(s, d) {
    return s.length === d.length && s.slice(0, -1).every( (f, m) => f === d[m]) ? s[s.length - 1] - d[d.length - 1] : 0
}
function Bg(s, d, o=!1) {
    let {routesMeta: f} = s
      , m = {}
      , g = "/"
      , p = [];
    for (let T = 0; T < f.length; ++T) {
        let S = f[T]
          , x = T === f.length - 1
          , N = g === "/" ? d : d.slice(g.length) || "/"
          , _ = di({
            path: S.relativePath,
            caseSensitive: S.caseSensitive,
            end: x
        }, N)
          , H = S.route;
        if (!_ && x && o && !f[f.length - 1].route.index && (_ = di({
            path: S.relativePath,
            caseSensitive: S.caseSensitive,
            end: !1
        }, N)),
        !_)
            return null;
        Object.assign(m, _.params),
        p.push({
            params: m,
            pathname: il([g, _.pathname]),
            pathnameBase: Vg(il([g, _.pathnameBase])),
            route: H
        }),
        _.pathnameBase !== "/" && (g = il([g, _.pathnameBase]))
    }
    return p
}
function di(s, d) {
    typeof s == "string" && (s = {
        path: s,
        caseSensitive: !1,
        end: !0
    });
    let[o,f] = Yg(s.path, s.caseSensitive, s.end)
      , m = d.match(o);
    if (!m)
        return null;
    let g = m[0]
      , p = g.replace(/(.)\/+$/, "$1")
      , T = m.slice(1);
    return {
        params: f.reduce( (x, {paramName: N, isOptional: _}, H) => {
            if (N === "*") {
                let L = T[H] || "";
                p = g.slice(0, g.length - L.length).replace(/(.)\/+$/, "$1")
            }
            const U = T[H];
            return _ && !U ? x[N] = void 0 : x[N] = (U || "").replace(/%2F/g, "/"),
            x
        }
        , {}),
        pathname: g,
        pathnameBase: p,
        pattern: s
    }
}
function Yg(s, d=!1, o=!0) {
    _e(s === "*" || !s.endsWith("*") || s.endsWith("/*"), `Route path "${s}" will be treated as if it were "${s.replace(/\*$/, "/*")}" because the \`*\` character must always follow a \`/\` in the pattern. To get rid of this warning, please change the route path to "${s.replace(/\*$/, "/*")}".`);
    let f = []
      , m = "^" + s.replace(/\/*\*?$/, "").replace(/^\/*/, "/").replace(/[\\.*+^${}|()[\]]/g, "\\$&").replace(/\/:([\w-]+)(\?)?/g, (p, T, S) => (f.push({
        paramName: T,
        isOptional: S != null
    }),
    S ? "/?([^\\/]+)?" : "/([^\\/]+)")).replace(/\/([\w-]+)\?(\/|$)/g, "(/$1)?$2");
    return s.endsWith("*") ? (f.push({
        paramName: "*"
    }),
    m += s === "*" || s === "/*" ? "(.*)$" : "(?:\\/(.+)|\\/*)$") : o ? m += "\\/*$" : s !== "" && s !== "/" && (m += "(?:(?=\\/|$))"),
    [new RegExp(m,d ? void 0 : "i"), f]
}
function Lg(s) {
    try {
        return s.split("/").map(d => decodeURIComponent(d).replace(/\//g, "%2F")).join("/")
    } catch (d) {
        return _e(!1, `The URL path "${s}" could not be decoded because it is a malformed URL segment. This is probably due to a bad percent encoding (${d}).`),
        s
    }
}
function cl(s, d) {
    if (d === "/")
        return s;
    if (!s.toLowerCase().startsWith(d.toLowerCase()))
        return null;
    let o = d.endsWith("/") ? d.length - 1 : d.length
      , f = s.charAt(o);
    return f && f !== "/" ? null : s.slice(o) || "/"
}
var Gg = /^(?:[a-z][a-z0-9+.-]*:|\/\/)/i
  , Xg = s => Gg.test(s);
function Qg(s, d="/") {
    let {pathname: o, search: f="", hash: m=""} = typeof s == "string" ? ea(s) : s, g;
    if (o)
        if (Xg(o))
            g = o;
        else {
            if (o.includes("//")) {
                let p = o;
                o = o.replace(/\/\/+/g, "/"),
                _e(!1, `Pathnames cannot have embedded double slashes - normalizing ${p} -> ${o}`)
            }
            o.startsWith("/") ? g = gm(o.substring(1), "/") : g = gm(o, d)
        }
    else
        g = d;
    return {
        pathname: g,
        search: Kg(f),
        hash: Jg(m)
    }
}
function gm(s, d) {
    let o = d.replace(/\/+$/, "").split("/");
    return s.split("/").forEach(m => {
        m === ".." ? o.length > 1 && o.pop() : m !== "." && o.push(m)
    }
    ),
    o.length > 1 ? o.join("/") : "/"
}
function Ls(s, d, o, f) {
    return `Cannot include a '${s}' character in a manually specified \`to.${d}\` field [${JSON.stringify(f)}].  Please separate it out to the \`to.${o}\` field. Alternatively you may provide the full path as a string in <Link to="..."> and the router will parse it for you.`
}
function Zg(s) {
    return s.filter( (d, o) => o === 0 || d.route.path && d.route.path.length > 0)
}
function zm(s) {
    let d = Zg(s);
    return d.map( (o, f) => f === d.length - 1 ? o.pathname : o.pathnameBase)
}
function Tm(s, d, o, f=!1) {
    let m;
    typeof s == "string" ? m = ea(s) : (m = {
        ...s
    },
    Et(!m.pathname || !m.pathname.includes("?"), Ls("?", "pathname", "search", m)),
    Et(!m.pathname || !m.pathname.includes("#"), Ls("#", "pathname", "hash", m)),
    Et(!m.search || !m.search.includes("#"), Ls("#", "search", "hash", m)));
    let g = s === "" || m.pathname === "", p = g ? "/" : m.pathname, T;
    if (p == null)
        T = o;
    else {
        let _ = d.length - 1;
        if (!f && p.startsWith("..")) {
            let H = p.split("/");
            for (; H[0] === ".."; )
                H.shift(),
                _ -= 1;
            m.pathname = H.join("/")
        }
        T = _ >= 0 ? d[_] : "/"
    }
    let S = Qg(m, T)
      , x = p && p !== "/" && p.endsWith("/")
      , N = (g || p === ".") && o.endsWith("/");
    return !S.pathname.endsWith("/") && (x || N) && (S.pathname += "/"),
    S
}
var il = s => s.join("/").replace(/\/\/+/g, "/")
  , Vg = s => s.replace(/\/+$/, "").replace(/^\/*/, "/")
  , Kg = s => !s || s === "?" ? "" : s.startsWith("?") ? s : "?" + s
  , Jg = s => !s || s === "#" ? "" : s.startsWith("#") ? s : "#" + s;
function kg(s) {
    return s != null && typeof s.status == "number" && typeof s.statusText == "string" && typeof s.internal == "boolean" && "data"in s
}
Object.getOwnPropertyNames(Object.prototype).sort().join("\0");
var Am = ["POST", "PUT", "PATCH", "DELETE"];
new Set(Am);
var $g = ["GET", ...Am];
new Set($g);
var Xa = M.createContext(null);
Xa.displayName = "DataRouter";
var mi = M.createContext(null);
mi.displayName = "DataRouterState";
M.createContext(!1);
var _m = M.createContext({
    isTransitioning: !1
});
_m.displayName = "ViewTransition";
var Wg = M.createContext(new Map);
Wg.displayName = "Fetchers";
var Fg = M.createContext(null);
Fg.displayName = "Await";
var Ye = M.createContext(null);
Ye.displayName = "Navigation";
var Gn = M.createContext(null);
Gn.displayName = "Location";
var Le = M.createContext({
    outlet: null,
    matches: [],
    isDataRoute: !1
});
Le.displayName = "Route";
var Vs = M.createContext(null);
Vs.displayName = "RouteError";
function Ig(s, {relative: d}={}) {
    Et(Xn(), "useHref() may be used only in the context of a <Router> component.");
    let {basename: o, navigator: f} = M.useContext(Ye)
      , {hash: m, pathname: g, search: p} = Qn(s, {
        relative: d
    })
      , T = g;
    return o !== "/" && (T = g === "/" ? o : il([o, g])),
    f.createHref({
        pathname: T,
        search: p,
        hash: m
    })
}
function Xn() {
    return M.useContext(Gn) != null
}
function sl() {
    return Et(Xn(), "useLocation() may be used only in the context of a <Router> component."),
    M.useContext(Gn).location
}
var Mm = "You should call navigate() in a React.useEffect(), not when your component is first rendered.";
function Om(s) {
    M.useContext(Ye).static || M.useLayoutEffect(s)
}
function Ks() {
    let {isDataRoute: s} = M.useContext(Le);
    return s ? d1() : Pg()
}
function Pg() {
    Et(Xn(), "useNavigate() may be used only in the context of a <Router> component.");
    let s = M.useContext(Xa)
      , {basename: d, navigator: o} = M.useContext(Ye)
      , {matches: f} = M.useContext(Le)
      , {pathname: m} = sl()
      , g = JSON.stringify(zm(f))
      , p = M.useRef(!1);
    return Om( () => {
        p.current = !0
    }
    ),
    M.useCallback( (S, x={}) => {
        if (_e(p.current, Mm),
        !p.current)
            return;
        if (typeof S == "number") {
            o.go(S);
            return
        }
        let N = Tm(S, JSON.parse(g), m, x.relative === "path");
        s == null && d !== "/" && (N.pathname = N.pathname === "/" ? d : il([d, N.pathname])),
        (x.replace ? o.replace : o.push)(N, x.state, x)
    }
    , [d, o, g, m, s])
}
M.createContext(null);
function t1() {
    let {matches: s} = M.useContext(Le)
      , d = s[s.length - 1];
    return d ? d.params : {}
}
function Qn(s, {relative: d}={}) {
    let {matches: o} = M.useContext(Le)
      , {pathname: f} = sl()
      , m = JSON.stringify(zm(o));
    return M.useMemo( () => Tm(s, JSON.parse(m), f, d === "path"), [s, m, f, d])
}
function e1(s, d) {
    return wm(s, d)
}
function wm(s, d, o, f, m) {
    var et;
    Et(Xn(), "useRoutes() may be used only in the context of a <Router> component.");
    let {navigator: g} = M.useContext(Ye)
      , {matches: p} = M.useContext(Le)
      , T = p[p.length - 1]
      , S = T ? T.params : {}
      , x = T ? T.pathname : "/"
      , N = T ? T.pathnameBase : "/"
      , _ = T && T.route;
    {
        let Y = _ && _.path || "";
        Dm(x, !_ || Y.endsWith("*") || Y.endsWith("*?"), `You rendered descendant <Routes> (or called \`useRoutes()\`) at "${x}" (under <Route path="${Y}">) but the parent route path has no trailing "*". This means if you navigate deeper, the parent won't match anymore and therefore the child routes will never render.

Please change the parent <Route path="${Y}"> to <Route path="${Y === "/" ? "*" : `${Y}/*`}">.`)
    }
    let H = sl(), U;
    if (d) {
        let Y = typeof d == "string" ? ea(d) : d;
        Et(N === "/" || ((et = Y.pathname) == null ? void 0 : et.startsWith(N)), `When overriding the location using \`<Routes location>\` or \`useRoutes(routes, location)\`, the location pathname must begin with the portion of the URL pathname that was matched by all parent routes. The current pathname base is "${N}" but pathname "${Y.pathname}" was given in the \`location\` prop.`),
        U = Y
    } else
        U = H;
    let L = U.pathname || "/"
      , J = L;
    if (N !== "/") {
        let Y = N.replace(/^\//, "").split("/");
        J = "/" + L.replace(/^\//, "").split("/").slice(Y.length).join("/")
    }
    let X = Nm(s, {
        pathname: J
    });
    _e(_ || X != null, `No routes matched location "${U.pathname}${U.search}${U.hash}" `),
    _e(X == null || X[X.length - 1].route.element !== void 0 || X[X.length - 1].route.Component !== void 0 || X[X.length - 1].route.lazy !== void 0, `Matched leaf route at location "${U.pathname}${U.search}${U.hash}" does not have an element or Component. This means it will render an <Outlet /> with a null value by default resulting in an "empty" page.`);
    let Z = i1(X && X.map(Y => Object.assign({}, Y, {
        params: Object.assign({}, S, Y.params),
        pathname: il([N, g.encodeLocation ? g.encodeLocation(Y.pathname.replace(/\?/g, "%3F").replace(/#/g, "%23")).pathname : Y.pathname]),
        pathnameBase: Y.pathnameBase === "/" ? N : il([N, g.encodeLocation ? g.encodeLocation(Y.pathnameBase.replace(/\?/g, "%3F").replace(/#/g, "%23")).pathname : Y.pathnameBase])
    })), p, o, f, m);
    return d && Z ? M.createElement(Gn.Provider, {
        value: {
            location: {
                pathname: "/",
                search: "",
                hash: "",
                state: null,
                key: "default",
                ...U
            },
            navigationType: "POP"
        }
    }, Z) : Z
}
function l1() {
    let s = o1()
      , d = kg(s) ? `${s.status} ${s.statusText}` : s instanceof Error ? s.message : JSON.stringify(s)
      , o = s instanceof Error ? s.stack : null
      , f = "rgba(200,200,200, 0.5)"
      , m = {
        padding: "0.5rem",
        backgroundColor: f
    }
      , g = {
        padding: "2px 4px",
        backgroundColor: f
    }
      , p = null;
    return console.error("Error handled by React Router default ErrorBoundary:", s),
    p = M.createElement(M.Fragment, null, M.createElement("p", null, "💿 Hey developer 👋"), M.createElement("p", null, "You can provide a way better UX than this when your app throws errors by providing your own ", M.createElement("code", {
        style: g
    }, "ErrorBoundary"), " or", " ", M.createElement("code", {
        style: g
    }, "errorElement"), " prop on your route.")),
    M.createElement(M.Fragment, null, M.createElement("h2", null, "Unexpected Application Error!"), M.createElement("h3", {
        style: {
            fontStyle: "italic"
        }
    }, d), o ? M.createElement("pre", {
        style: m
    }, o) : null, p)
}
var a1 = M.createElement(l1, null)
  , n1 = class extends M.Component {
    constructor(s) {
        super(s),
        this.state = {
            location: s.location,
            revalidation: s.revalidation,
            error: s.error
        }
    }
    static getDerivedStateFromError(s) {
        return {
            error: s
        }
    }
    static getDerivedStateFromProps(s, d) {
        return d.location !== s.location || d.revalidation !== "idle" && s.revalidation === "idle" ? {
            error: s.error,
            location: s.location,
            revalidation: s.revalidation
        } : {
            error: s.error !== void 0 ? s.error : d.error,
            location: d.location,
            revalidation: s.revalidation || d.revalidation
        }
    }
    componentDidCatch(s, d) {
        this.props.onError ? this.props.onError(s, d) : console.error("React Router caught the following error during render", s)
    }
    render() {
        return this.state.error !== void 0 ? M.createElement(Le.Provider, {
            value: this.props.routeContext
        }, M.createElement(Vs.Provider, {
            value: this.state.error,
            children: this.props.component
        })) : this.props.children
    }
}
;
function u1({routeContext: s, match: d, children: o}) {
    let f = M.useContext(Xa);
    return f && f.static && f.staticContext && (d.route.errorElement || d.route.ErrorBoundary) && (f.staticContext._deepestRenderedBoundaryId = d.route.id),
    M.createElement(Le.Provider, {
        value: s
    }, o)
}
function i1(s, d=[], o=null, f=null, m=null) {
    if (s == null) {
        if (!o)
            return null;
        if (o.errors)
            s = o.matches;
        else if (d.length === 0 && !o.initialized && o.matches.length > 0)
            s = o.matches;
        else
            return null
    }
    let g = s
      , p = o == null ? void 0 : o.errors;
    if (p != null) {
        let N = g.findIndex(_ => _.route.id && (p == null ? void 0 : p[_.route.id]) !== void 0);
        Et(N >= 0, `Could not find a matching route for errors on route IDs: ${Object.keys(p).join(",")}`),
        g = g.slice(0, Math.min(g.length, N + 1))
    }
    let T = !1
      , S = -1;
    if (o)
        for (let N = 0; N < g.length; N++) {
            let _ = g[N];
            if ((_.route.HydrateFallback || _.route.hydrateFallbackElement) && (S = N),
            _.route.id) {
                let {loaderData: H, errors: U} = o
                  , L = _.route.loader && !H.hasOwnProperty(_.route.id) && (!U || U[_.route.id] === void 0);
                if (_.route.lazy || L) {
                    T = !0,
                    S >= 0 ? g = g.slice(0, S + 1) : g = [g[0]];
                    break
                }
            }
        }
    let x = o && f ? (N, _) => {
        var H, U;
        f(N, {
            location: o.location,
            params: ((U = (H = o.matches) == null ? void 0 : H[0]) == null ? void 0 : U.params) ?? {},
            errorInfo: _
        })
    }
    : void 0;
    return g.reduceRight( (N, _, H) => {
        let U, L = !1, J = null, X = null;
        o && (U = p && _.route.id ? p[_.route.id] : void 0,
        J = _.route.errorElement || a1,
        T && (S < 0 && H === 0 ? (Dm("route-fallback", !1, "No `HydrateFallback` element provided to render during initial hydration"),
        L = !0,
        X = null) : S === H && (L = !0,
        X = _.route.hydrateFallbackElement || null)));
        let Z = d.concat(g.slice(0, H + 1))
          , et = () => {
            let Y;
            return U ? Y = J : L ? Y = X : _.route.Component ? Y = M.createElement(_.route.Component, null) : _.route.element ? Y = _.route.element : Y = N,
            M.createElement(u1, {
                match: _,
                routeContext: {
                    outlet: N,
                    matches: Z,
                    isDataRoute: o != null
                },
                children: Y
            })
        }
        ;
        return o && (_.route.ErrorBoundary || _.route.errorElement || H === 0) ? M.createElement(n1, {
            location: o.location,
            revalidation: o.revalidation,
            component: J,
            error: U,
            children: et(),
            routeContext: {
                outlet: null,
                matches: Z,
                isDataRoute: !0
            },
            onError: x
        }) : et()
    }
    , null)
}
function Js(s) {
    return `${s} must be used within a data router.  See https://reactrouter.com/en/main/routers/picking-a-router.`
}
function c1(s) {
    let d = M.useContext(Xa);
    return Et(d, Js(s)),
    d
}
function s1(s) {
    let d = M.useContext(mi);
    return Et(d, Js(s)),
    d
}
function f1(s) {
    let d = M.useContext(Le);
    return Et(d, Js(s)),
    d
}
function ks(s) {
    let d = f1(s)
      , o = d.matches[d.matches.length - 1];
    return Et(o.route.id, `${s} can only be used on routes that contain a unique "id"`),
    o.route.id
}
function r1() {
    return ks("useRouteId")
}
function o1() {
    var f;
    let s = M.useContext(Vs)
      , d = s1("useRouteError")
      , o = ks("useRouteError");
    return s !== void 0 ? s : (f = d.errors) == null ? void 0 : f[o]
}
function d1() {
    let {router: s} = c1("useNavigate")
      , d = ks("useNavigate")
      , o = M.useRef(!1);
    return Om( () => {
        o.current = !0
    }
    ),
    M.useCallback(async (m, g={}) => {
        _e(o.current, Mm),
        o.current && (typeof m == "number" ? s.navigate(m) : await s.navigate(m, {
            fromRouteId: d,
            ...g
        }))
    }
    , [s, d])
}
var xm = {};
function Dm(s, d, o) {
    !d && !xm[s] && (xm[s] = !0,
    _e(!1, o))
}
M.memo(m1);
function m1({routes: s, future: d, state: o, unstable_onError: f}) {
    return wm(s, void 0, o, f, d)
}
function Be(s) {
    Et(!1, "A <Route> is only ever to be used as the child of <Routes> element, never rendered directly. Please wrap your <Route> in a <Routes>.")
}
function h1({basename: s="/", children: d=null, location: o, navigationType: f="POP", navigator: m, static: g=!1}) {
    Et(!Xn(), "You cannot render a <Router> inside another <Router>. You should never have more than one in your app.");
    let p = s.replace(/^\/*/, "/")
      , T = M.useMemo( () => ({
        basename: p,
        navigator: m,
        static: g,
        future: {}
    }), [p, m, g]);
    typeof o == "string" && (o = ea(o));
    let {pathname: S="/", search: x="", hash: N="", state: _=null, key: H="default"} = o
      , U = M.useMemo( () => {
        let L = cl(S, p);
        return L == null ? null : {
            location: {
                pathname: L,
                search: x,
                hash: N,
                state: _,
                key: H
            },
            navigationType: f
        }
    }
    , [p, S, x, N, _, H, f]);
    return _e(U != null, `<Router basename="${p}"> is not able to match the URL "${S}${x}${N}" because it does not start with the basename, so the <Router> won't render anything.`),
    U == null ? null : M.createElement(Ye.Provider, {
        value: T
    }, M.createElement(Gn.Provider, {
        children: d,
        value: U
    }))
}
function g1({children: s, location: d}) {
    return e1(Qs(s), d)
}
function Qs(s, d=[]) {
    let o = [];
    return M.Children.forEach(s, (f, m) => {
        if (!M.isValidElement(f))
            return;
        let g = [...d, m];
        if (f.type === M.Fragment) {
            o.push.apply(o, Qs(f.props.children, g));
            return
        }
        Et(f.type === Be, `[${typeof f.type == "string" ? f.type : f.type.name}] is not a <Route> component. All component children of <Routes> must be a <Route> or <React.Fragment>`),
        Et(!f.props.index || !f.props.children, "An index route cannot have child routes.");
        let p = {
            id: f.props.id || g.join("-"),
            caseSensitive: f.props.caseSensitive,
            element: f.props.element,
            Component: f.props.Component,
            index: f.props.index,
            path: f.props.path,
            middleware: f.props.middleware,
            loader: f.props.loader,
            action: f.props.action,
            hydrateFallbackElement: f.props.hydrateFallbackElement,
            HydrateFallback: f.props.HydrateFallback,
            errorElement: f.props.errorElement,
            ErrorBoundary: f.props.ErrorBoundary,
            hasErrorBoundary: f.props.hasErrorBoundary === !0 || f.props.ErrorBoundary != null || f.props.errorElement != null,
            shouldRevalidate: f.props.shouldRevalidate,
            handle: f.props.handle,
            lazy: f.props.lazy
        };
        f.props.children && (p.children = Qs(f.props.children, g)),
        o.push(p)
    }
    ),
    o
}
var fi = "get"
  , ri = "application/x-www-form-urlencoded";
function hi(s) {
    return s != null && typeof s.tagName == "string"
}
function x1(s) {
    return hi(s) && s.tagName.toLowerCase() === "button"
}
function y1(s) {
    return hi(s) && s.tagName.toLowerCase() === "form"
}
function v1(s) {
    return hi(s) && s.tagName.toLowerCase() === "input"
}
function p1(s) {
    return !!(s.metaKey || s.altKey || s.ctrlKey || s.shiftKey)
}
function b1(s, d) {
    return s.button === 0 && (!d || d === "_self") && !p1(s)
}
var si = null;
function S1() {
    if (si === null)
        try {
            new FormData(document.createElement("form"),0),
            si = !1
        } catch {
            si = !0
        }
    return si
}
var N1 = new Set(["application/x-www-form-urlencoded", "multipart/form-data", "text/plain"]);
function Gs(s) {
    return s != null && !N1.has(s) ? (_e(!1, `"${s}" is not a valid \`encType\` for \`<Form>\`/\`<fetcher.Form>\` and will default to "${ri}"`),
    null) : s
}
function j1(s, d) {
    let o, f, m, g, p;
    if (y1(s)) {
        let T = s.getAttribute("action");
        f = T ? cl(T, d) : null,
        o = s.getAttribute("method") || fi,
        m = Gs(s.getAttribute("enctype")) || ri,
        g = new FormData(s)
    } else if (x1(s) || v1(s) && (s.type === "submit" || s.type === "image")) {
        let T = s.form;
        if (T == null)
            throw new Error('Cannot submit a <button> or <input type="submit"> without a <form>');
        let S = s.getAttribute("formaction") || T.getAttribute("action");
        if (f = S ? cl(S, d) : null,
        o = s.getAttribute("formmethod") || T.getAttribute("method") || fi,
        m = Gs(s.getAttribute("formenctype")) || Gs(T.getAttribute("enctype")) || ri,
        g = new FormData(T,s),
        !S1()) {
            let {name: x, type: N, value: _} = s;
            if (N === "image") {
                let H = x ? `${x}.` : "";
                g.append(`${H}x`, "0"),
                g.append(`${H}y`, "0")
            } else
                x && g.append(x, _)
        }
    } else {
        if (hi(s))
            throw new Error('Cannot submit element that is not <form>, <button>, or <input type="submit|image">');
        o = fi,
        f = null,
        m = ri,
        p = s
    }
    return g && m === "text/plain" && (p = g,
    g = void 0),
    {
        action: f,
        method: o.toLowerCase(),
        encType: m,
        formData: g,
        body: p
    }
}
Object.getOwnPropertyNames(Object.prototype).sort().join("\0");
function $s(s, d) {
    if (s === !1 || s === null || typeof s > "u")
        throw new Error(d)
}
function E1(s, d, o) {
    let f = typeof s == "string" ? new URL(s,typeof window > "u" ? "server://singlefetch/" : window.location.origin) : s;
    return f.pathname === "/" ? f.pathname = `_root.${o}` : d && cl(f.pathname, d) === "/" ? f.pathname = `${d.replace(/\/$/, "")}/_root.${o}` : f.pathname = `${f.pathname.replace(/\/$/, "")}.${o}`,
    f
}
async function z1(s, d) {
    if (s.id in d)
        return d[s.id];
    try {
        let o = await import(s.module);
        return d[s.id] = o,
        o
    } catch (o) {
        return console.error(`Error loading route module \`${s.module}\`, reloading page...`),
        console.error(o),
        window.__reactRouterContext && window.__reactRouterContext.isSpaMode,
        window.location.reload(),
        new Promise( () => {}
        )
    }
}
function T1(s) {
    return s == null ? !1 : s.href == null ? s.rel === "preload" && typeof s.imageSrcSet == "string" && typeof s.imageSizes == "string" : typeof s.rel == "string" && typeof s.href == "string"
}
async function A1(s, d, o) {
    let f = await Promise.all(s.map(async m => {
        let g = d.routes[m.route.id];
        if (g) {
            let p = await z1(g, o);
            return p.links ? p.links() : []
        }
        return []
    }
    ));
    return w1(f.flat(1).filter(T1).filter(m => m.rel === "stylesheet" || m.rel === "preload").map(m => m.rel === "stylesheet" ? {
        ...m,
        rel: "prefetch",
        as: "style"
    } : {
        ...m,
        rel: "prefetch"
    }))
}
function ym(s, d, o, f, m, g) {
    let p = (S, x) => o[x] ? S.route.id !== o[x].route.id : !0
      , T = (S, x) => {
        var N;
        return o[x].pathname !== S.pathname || ((N = o[x].route.path) == null ? void 0 : N.endsWith("*")) && o[x].params["*"] !== S.params["*"]
    }
    ;
    return g === "assets" ? d.filter( (S, x) => p(S, x) || T(S, x)) : g === "data" ? d.filter( (S, x) => {
        var _;
        let N = f.routes[S.route.id];
        if (!N || !N.hasLoader)
            return !1;
        if (p(S, x) || T(S, x))
            return !0;
        if (S.route.shouldRevalidate) {
            let H = S.route.shouldRevalidate({
                currentUrl: new URL(m.pathname + m.search + m.hash,window.origin),
                currentParams: ((_ = o[0]) == null ? void 0 : _.params) || {},
                nextUrl: new URL(s,window.origin),
                nextParams: S.params,
                defaultShouldRevalidate: !0
            });
            if (typeof H == "boolean")
                return H
        }
        return !0
    }
    ) : []
}
function _1(s, d, {includeHydrateFallback: o}={}) {
    return M1(s.map(f => {
        let m = d.routes[f.route.id];
        if (!m)
            return [];
        let g = [m.module];
        return m.clientActionModule && (g = g.concat(m.clientActionModule)),
        m.clientLoaderModule && (g = g.concat(m.clientLoaderModule)),
        o && m.hydrateFallbackModule && (g = g.concat(m.hydrateFallbackModule)),
        m.imports && (g = g.concat(m.imports)),
        g
    }
    ).flat(1))
}
function M1(s) {
    return [...new Set(s)]
}
function O1(s) {
    let d = {}
      , o = Object.keys(s).sort();
    for (let f of o)
        d[f] = s[f];
    return d
}
function w1(s, d) {
    let o = new Set;
    return new Set(d),
    s.reduce( (f, m) => {
        let g = JSON.stringify(O1(m));
        return o.has(g) || (o.add(g),
        f.push({
            key: g,
            link: m
        })),
        f
    }
    , [])
}
function Cm() {
    let s = M.useContext(Xa);
    return $s(s, "You must render this element inside a <DataRouterContext.Provider> element"),
    s
}
function D1() {
    let s = M.useContext(mi);
    return $s(s, "You must render this element inside a <DataRouterStateContext.Provider> element"),
    s
}
var Ws = M.createContext(void 0);
Ws.displayName = "FrameworkContext";
function Rm() {
    let s = M.useContext(Ws);
    return $s(s, "You must render this element inside a <HydratedRouter> element"),
    s
}
function C1(s, d) {
    let o = M.useContext(Ws)
      , [f,m] = M.useState(!1)
      , [g,p] = M.useState(!1)
      , {onFocus: T, onBlur: S, onMouseEnter: x, onMouseLeave: N, onTouchStart: _} = d
      , H = M.useRef(null);
    M.useEffect( () => {
        if (s === "render" && p(!0),
        s === "viewport") {
            let J = Z => {
                Z.forEach(et => {
                    p(et.isIntersecting)
                }
                )
            }
              , X = new IntersectionObserver(J,{
                threshold: .5
            });
            return H.current && X.observe(H.current),
            () => {
                X.disconnect()
            }
        }
    }
    , [s]),
    M.useEffect( () => {
        if (f) {
            let J = setTimeout( () => {
                p(!0)
            }
            , 100);
            return () => {
                clearTimeout(J)
            }
        }
    }
    , [f]);
    let U = () => {
        m(!0)
    }
      , L = () => {
        m(!1),
        p(!1)
    }
    ;
    return o ? s !== "intent" ? [g, H, {}] : [g, H, {
        onFocus: Yn(T, U),
        onBlur: Yn(S, L),
        onMouseEnter: Yn(x, U),
        onMouseLeave: Yn(N, L),
        onTouchStart: Yn(_, U)
    }] : [!1, H, {}]
}
function Yn(s, d) {
    return o => {
        s && s(o),
        o.defaultPrevented || d(o)
    }
}
function R1({page: s, ...d}) {
    let {router: o} = Cm()
      , f = M.useMemo( () => Nm(o.routes, s, o.basename), [o.routes, s, o.basename]);
    return f ? M.createElement(H1, {
        page: s,
        matches: f,
        ...d
    }) : null
}
function U1(s) {
    let {manifest: d, routeModules: o} = Rm()
      , [f,m] = M.useState([]);
    return M.useEffect( () => {
        let g = !1;
        return A1(s, d, o).then(p => {
            g || m(p)
        }
        ),
        () => {
            g = !0
        }
    }
    , [s, d, o]),
    f
}
function H1({page: s, matches: d, ...o}) {
    let f = sl()
      , {manifest: m, routeModules: g} = Rm()
      , {basename: p} = Cm()
      , {loaderData: T, matches: S} = D1()
      , x = M.useMemo( () => ym(s, d, S, m, f, "data"), [s, d, S, m, f])
      , N = M.useMemo( () => ym(s, d, S, m, f, "assets"), [s, d, S, m, f])
      , _ = M.useMemo( () => {
        if (s === f.pathname + f.search + f.hash)
            return [];
        let L = new Set
          , J = !1;
        if (d.forEach(Z => {
            var Y;
            let et = m.routes[Z.route.id];
            !et || !et.hasLoader || (!x.some(dt => dt.route.id === Z.route.id) && Z.route.id in T && ((Y = g[Z.route.id]) != null && Y.shouldRevalidate) || et.hasClientLoader ? J = !0 : L.add(Z.route.id))
        }
        ),
        L.size === 0)
            return [];
        let X = E1(s, p, "data");
        return J && L.size > 0 && X.searchParams.set("_routes", d.filter(Z => L.has(Z.route.id)).map(Z => Z.route.id).join(",")),
        [X.pathname + X.search]
    }
    , [p, T, f, m, x, d, s, g])
      , H = M.useMemo( () => _1(N, m), [N, m])
      , U = U1(N);
    return M.createElement(M.Fragment, null, _.map(L => M.createElement("link", {
        key: L,
        rel: "prefetch",
        as: "fetch",
        href: L,
        ...o
    })), H.map(L => M.createElement("link", {
        key: L,
        rel: "modulepreload",
        href: L,
        ...o
    })), U.map( ({key: L, link: J}) => M.createElement("link", {
        key: L,
        nonce: o.nonce,
        ...J
    })))
}
function q1(...s) {
    return d => {
        s.forEach(o => {
            typeof o == "function" ? o(d) : o != null && (o.current = d)
        }
        )
    }
}
var Um = typeof window < "u" && typeof window.document < "u" && typeof window.document.createElement < "u";
try {
    Um && (window.__reactRouterVersion = "7.9.6")
} catch {}
function B1({basename: s, children: d, window: o}) {
    let f = M.useRef();
    f.current == null && (f.current = Eg({
        window: o,
        v5Compat: !0
    }));
    let m = f.current
      , [g,p] = M.useState({
        action: m.action,
        location: m.location
    })
      , T = M.useCallback(S => {
        M.startTransition( () => p(S))
    }
    , [p]);
    return M.useLayoutEffect( () => m.listen(T), [m, T]),
    M.createElement(h1, {
        basename: s,
        children: d,
        location: g.location,
        navigationType: g.action,
        navigator: m
    })
}
var Hm = /^(?:[a-z][a-z0-9+.-]*:|\/\/)/i
  , Lt = M.forwardRef(function({onClick: d, discover: o="render", prefetch: f="none", relative: m, reloadDocument: g, replace: p, state: T, target: S, to: x, preventScrollReset: N, viewTransition: _, ...H}, U) {
    let {basename: L} = M.useContext(Ye), J = typeof x == "string" && Hm.test(x), X, Z = !1;
    if (typeof x == "string" && J && (X = x,
    Um))
        try {
            let Tt = new URL(window.location.href)
              , ie = x.startsWith("//") ? new URL(Tt.protocol + x) : new URL(x)
              , ce = cl(ie.pathname, L);
            ie.origin === Tt.origin && ce != null ? x = ce + ie.search + ie.hash : Z = !0
        } catch {
            _e(!1, `<Link to="${x}"> contains an invalid URL which will probably break when clicked - please update to a valid URL path.`)
        }
    let et = Ig(x, {
        relative: m
    })
      , [Y,dt,zt] = C1(f, H)
      , qt = X1(x, {
        replace: p,
        state: T,
        target: S,
        preventScrollReset: N,
        relative: m,
        viewTransition: _
    });
    function P(Tt) {
        d && d(Tt),
        Tt.defaultPrevented || qt(Tt)
    }
    let Bt = M.createElement("a", {
        ...H,
        ...zt,
        href: X || et,
        onClick: Z || g ? d : P,
        ref: q1(U, dt),
        target: S,
        "data-discover": !J && o === "render" ? "true" : void 0
    });
    return Y && !J ? M.createElement(M.Fragment, null, Bt, M.createElement(R1, {
        page: et
    })) : Bt
});
Lt.displayName = "Link";
var Y1 = M.forwardRef(function({"aria-current": d="page", caseSensitive: o=!1, className: f="", end: m=!1, style: g, to: p, viewTransition: T, children: S, ...x}, N) {
    let _ = Qn(p, {
        relative: x.relative
    })
      , H = sl()
      , U = M.useContext(mi)
      , {navigator: L, basename: J} = M.useContext(Ye)
      , X = U != null && J1(_) && T === !0
      , Z = L.encodeLocation ? L.encodeLocation(_).pathname : _.pathname
      , et = H.pathname
      , Y = U && U.navigation && U.navigation.location ? U.navigation.location.pathname : null;
    o || (et = et.toLowerCase(),
    Y = Y ? Y.toLowerCase() : null,
    Z = Z.toLowerCase()),
    Y && J && (Y = cl(Y, J) || Y);
    const dt = Z !== "/" && Z.endsWith("/") ? Z.length - 1 : Z.length;
    let zt = et === Z || !m && et.startsWith(Z) && et.charAt(dt) === "/", qt = Y != null && (Y === Z || !m && Y.startsWith(Z) && Y.charAt(Z.length) === "/"), P = {
        isActive: zt,
        isPending: qt,
        isTransitioning: X
    }, Bt = zt ? d : void 0, Tt;
    typeof f == "function" ? Tt = f(P) : Tt = [f, zt ? "active" : null, qt ? "pending" : null, X ? "transitioning" : null].filter(Boolean).join(" ");
    let ie = typeof g == "function" ? g(P) : g;
    return M.createElement(Lt, {
        ...x,
        "aria-current": Bt,
        className: Tt,
        ref: N,
        style: ie,
        to: p,
        viewTransition: T
    }, typeof S == "function" ? S(P) : S)
});
Y1.displayName = "NavLink";
var L1 = M.forwardRef( ({discover: s="render", fetcherKey: d, navigate: o, reloadDocument: f, replace: m, state: g, method: p=fi, action: T, onSubmit: S, relative: x, preventScrollReset: N, viewTransition: _, ...H}, U) => {
    let L = V1()
      , J = K1(T, {
        relative: x
    })
      , X = p.toLowerCase() === "get" ? "get" : "post"
      , Z = typeof T == "string" && Hm.test(T)
      , et = Y => {
        if (S && S(Y),
        Y.defaultPrevented)
            return;
        Y.preventDefault();
        let dt = Y.nativeEvent.submitter
          , zt = (dt == null ? void 0 : dt.getAttribute("formmethod")) || p;
        L(dt || Y.currentTarget, {
            fetcherKey: d,
            method: zt,
            navigate: o,
            replace: m,
            state: g,
            relative: x,
            preventScrollReset: N,
            viewTransition: _
        })
    }
    ;
    return M.createElement("form", {
        ref: U,
        method: X,
        action: J,
        onSubmit: f ? S : et,
        ...H,
        "data-discover": !Z && s === "render" ? "true" : void 0
    })
}
);
L1.displayName = "Form";
function G1(s) {
    return `${s} must be used within a data router.  See https://reactrouter.com/en/main/routers/picking-a-router.`
}
function qm(s) {
    let d = M.useContext(Xa);
    return Et(d, G1(s)),
    d
}
function X1(s, {target: d, replace: o, state: f, preventScrollReset: m, relative: g, viewTransition: p}={}) {
    let T = Ks()
      , S = sl()
      , x = Qn(s, {
        relative: g
    });
    return M.useCallback(N => {
        if (b1(N, d)) {
            N.preventDefault();
            let _ = o !== void 0 ? o : Ln(S) === Ln(x);
            T(s, {
                replace: _,
                state: f,
                preventScrollReset: m,
                relative: g,
                viewTransition: p
            })
        }
    }
    , [S, T, x, o, f, d, s, m, g, p])
}
var Q1 = 0
  , Z1 = () => `__${String(++Q1)}__`;
function V1() {
    let {router: s} = qm("useSubmit")
      , {basename: d} = M.useContext(Ye)
      , o = r1();
    return M.useCallback(async (f, m={}) => {
        let {action: g, method: p, encType: T, formData: S, body: x} = j1(f, d);
        if (m.navigate === !1) {
            let N = m.fetcherKey || Z1();
            await s.fetch(N, o, m.action || g, {
                preventScrollReset: m.preventScrollReset,
                formData: S,
                body: x,
                formMethod: m.method || p,
                formEncType: m.encType || T,
                flushSync: m.flushSync
            })
        } else
            await s.navigate(m.action || g, {
                preventScrollReset: m.preventScrollReset,
                formData: S,
                body: x,
                formMethod: m.method || p,
                formEncType: m.encType || T,
                replace: m.replace,
                state: m.state,
                fromRouteId: o,
                flushSync: m.flushSync,
                viewTransition: m.viewTransition
            })
    }
    , [s, d, o])
}
function K1(s, {relative: d}={}) {
    let {basename: o} = M.useContext(Ye)
      , f = M.useContext(Le);
    Et(f, "useFormAction must be used inside a RouteContext");
    let[m] = f.matches.slice(-1)
      , g = {
        ...Qn(s || ".", {
            relative: d
        })
    }
      , p = sl();
    if (s == null) {
        g.search = p.search;
        let T = new URLSearchParams(g.search)
          , S = T.getAll("index");
        if (S.some(N => N === "")) {
            T.delete("index"),
            S.filter(_ => _).forEach(_ => T.append("index", _));
            let N = T.toString();
            g.search = N ? `?${N}` : ""
        }
    }
    return (!s || s === ".") && m.route.index && (g.search = g.search ? g.search.replace(/^\?/, "?index&") : "?index"),
    o !== "/" && (g.pathname = g.pathname === "/" ? o : il([o, g.pathname])),
    Ln(g)
}
function J1(s, {relative: d}={}) {
    let o = M.useContext(_m);
    Et(o != null, "`useViewTransitionState` must be used within `react-router-dom`'s `RouterProvider`.  Did you accidentally import `RouterProvider` from `react-router`?");
    let {basename: f} = qm("useViewTransitionState")
      , m = Qn(s, {
        relative: d
    });
    if (!o.isTransitioning)
        return !1;
    let g = cl(o.currentLocation.pathname, f) || o.currentLocation.pathname
      , p = cl(o.nextLocation.pathname, f) || o.nextLocation.pathname;
    return di(m.pathname, p) != null || di(m.pathname, g) != null
}
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const k1 = s => s.replace(/([a-z0-9])([A-Z])/g, "$1-$2").toLowerCase()
  , $1 = s => s.replace(/^([A-Z])|[\s-_]+(\w)/g, (d, o, f) => f ? f.toUpperCase() : o.toLowerCase())
  , vm = s => {
    const d = $1(s);
    return d.charAt(0).toUpperCase() + d.slice(1)
}
  , Bm = (...s) => s.filter( (d, o, f) => !!d && d.trim() !== "" && f.indexOf(d) === o).join(" ").trim()
  , W1 = s => {
    for (const d in s)
        if (d.startsWith("aria-") || d === "role" || d === "title")
            return !0
}
;
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
var F1 = {
    xmlns: "http://www.w3.org/2000/svg",
    width: 24,
    height: 24,
    viewBox: "0 0 24 24",
    fill: "none",
    stroke: "currentColor",
    strokeWidth: 2,
    strokeLinecap: "round",
    strokeLinejoin: "round"
};
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const I1 = M.forwardRef( ({color: s="currentColor", size: d=24, strokeWidth: o=2, absoluteStrokeWidth: f, className: m="", children: g, iconNode: p, ...T}, S) => M.createElement("svg", {
    ref: S,
    ...F1,
    width: d,
    height: d,
    stroke: s,
    strokeWidth: f ? Number(o) * 24 / Number(d) : o,
    className: Bm("lucide", m),
    ...!g && !W1(T) && {
        "aria-hidden": "true"
    },
    ...T
}, [...p.map( ([x,N]) => M.createElement(x, N)), ...Array.isArray(g) ? g : [g]]));
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Mt = (s, d) => {
    const o = M.forwardRef( ({className: f, ...m}, g) => M.createElement(I1, {
        ref: g,
        iconNode: d,
        className: Bm(`lucide-${k1(vm(s))}`, `lucide-${s}`, f),
        ...m
    }));
    return o.displayName = vm(s),
    o
}
;
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const P1 = [["path", {
    d: "m12 19-7-7 7-7",
    key: "1l729n"
}], ["path", {
    d: "M19 12H5",
    key: "x3x0zl"
}]]
  , Ym = Mt("arrow-left", P1);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const tx = [["path", {
    d: "M5 12h14",
    key: "1ays0h"
}], ["path", {
    d: "m12 5 7 7-7 7",
    key: "xquz4c"
}]]
  , ex = Mt("arrow-right", tx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const lx = [["path", {
    d: "M8 2v4",
    key: "1cmpym"
}], ["path", {
    d: "M16 2v4",
    key: "4m81vk"
}], ["rect", {
    width: "18",
    height: "18",
    x: "3",
    y: "4",
    rx: "2",
    key: "1hopcy"
}], ["path", {
    d: "M3 10h18",
    key: "8toen8"
}]]
  , gi = Mt("calendar", lx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const ax = [["path", {
    d: "M21.801 10A10 10 0 1 1 17 3.335",
    key: "yps3ct"
}], ["path", {
    d: "m9 11 3 3L22 4",
    key: "1pflzl"
}]]
  , La = Mt("circle-check-big", ax);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const nx = [["path", {
    d: "M12 6v6l4 2",
    key: "mmk7yg"
}], ["circle", {
    cx: "12",
    cy: "12",
    r: "10",
    key: "1mglay"
}]]
  , Fs = Mt("clock", nx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const ux = [["path", {
    d: "m16 18 6-6-6-6",
    key: "eg8j8"
}], ["path", {
    d: "m8 6-6 6 6 6",
    key: "ppft3o"
}]]
  , ix = Mt("code", ux);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const cx = [["path", {
    d: "M10 20a1 1 0 0 0 .553.895l2 1A1 1 0 0 0 14 21v-7a2 2 0 0 1 .517-1.341L21.74 4.67A1 1 0 0 0 21 3H3a1 1 0 0 0-.742 1.67l7.225 7.989A2 2 0 0 1 10 14z",
    key: "sc7q7i"
}]]
  , sx = Mt("funnel", cx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const fx = [["path", {
    d: "M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4",
    key: "tonef"
}], ["path", {
    d: "M9 18c-4.51 2-5-2-7-2",
    key: "9comsn"
}]]
  , rx = Mt("github", fx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const ox = [["path", {
    d: "M15 21v-8a1 1 0 0 0-1-1h-4a1 1 0 0 0-1 1v8",
    key: "5wwlr5"
}], ["path", {
    d: "M3 10a2 2 0 0 1 .709-1.528l7-6a2 2 0 0 1 2.582 0l7 6A2 2 0 0 1 21 10v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z",
    key: "r6nss1"
}]]
  , dx = Mt("house", ox);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const mx = [["rect", {
    width: "20",
    height: "20",
    x: "2",
    y: "2",
    rx: "5",
    ry: "5",
    key: "2e1cvw"
}], ["path", {
    d: "M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z",
    key: "9exkf1"
}], ["line", {
    x1: "17.5",
    x2: "17.51",
    y1: "6.5",
    y2: "6.5",
    key: "r4j83e"
}]]
  , hx = Mt("instagram", mx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const gx = [["path", {
    d: "m22 7-8.991 5.727a2 2 0 0 1-2.009 0L2 7",
    key: "132q7q"
}], ["rect", {
    x: "2",
    y: "4",
    width: "20",
    height: "16",
    rx: "2",
    key: "izxlao"
}]]
  , xx = Mt("mail", gx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const yx = [["path", {
    d: "M20 10c0 4.993-5.539 10.193-7.399 11.799a1 1 0 0 1-1.202 0C9.539 20.193 4 14.993 4 10a8 8 0 0 1 16 0",
    key: "1r0f0z"
}], ["circle", {
    cx: "12",
    cy: "10",
    r: "3",
    key: "ilqhr7"
}]]
  , ta = Mt("map-pin", yx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const vx = [["path", {
    d: "M4 5h16",
    key: "1tepv9"
}], ["path", {
    d: "M4 12h16",
    key: "1lakjw"
}], ["path", {
    d: "M4 19h16",
    key: "1djgab"
}]]
  , px = Mt("menu", vx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const bx = [["rect", {
    width: "18",
    height: "18",
    x: "3",
    y: "3",
    rx: "2",
    key: "afitv7"
}], ["path", {
    d: "M3 9h18",
    key: "1pudct"
}], ["path", {
    d: "M9 21V9",
    key: "1oto5p"
}]]
  , Sx = Mt("panels-top-left", bx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Nx = [["path", {
    d: "m21 21-4.34-4.34",
    key: "14j7rj"
}], ["circle", {
    cx: "11",
    cy: "11",
    r: "8",
    key: "4ej97u"
}]]
  , jx = Mt("search", Nx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Ex = [["circle", {
    cx: "18",
    cy: "5",
    r: "3",
    key: "gq8acd"
}], ["circle", {
    cx: "6",
    cy: "12",
    r: "3",
    key: "w7nqdw"
}], ["circle", {
    cx: "18",
    cy: "19",
    r: "3",
    key: "1xt0gg"
}], ["line", {
    x1: "8.59",
    x2: "15.42",
    y1: "13.51",
    y2: "17.49",
    key: "47mynk"
}], ["line", {
    x1: "15.41",
    x2: "8.59",
    y1: "6.51",
    y2: "10.49",
    key: "1n3mei"
}]]
  , zx = Mt("share-2", Ex);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Tx = [["path", {
    d: "M11.525 2.295a.53.53 0 0 1 .95 0l2.31 4.679a2.123 2.123 0 0 0 1.595 1.16l5.166.756a.53.53 0 0 1 .294.904l-3.736 3.638a2.123 2.123 0 0 0-.611 1.878l.882 5.14a.53.53 0 0 1-.771.56l-4.618-2.428a2.122 2.122 0 0 0-1.973 0L6.396 21.01a.53.53 0 0 1-.77-.56l.881-5.139a2.122 2.122 0 0 0-.611-1.879L2.16 9.795a.53.53 0 0 1 .294-.906l5.165-.755a2.122 2.122 0 0 0 1.597-1.16z",
    key: "r04s7s"
}]]
  , Lm = Mt("star", Tx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Ax = [["path", {
    d: "M12 19h8",
    key: "baeox8"
}], ["path", {
    d: "m4 17 6-6-6-6",
    key: "1yngyt"
}]]
  , _x = Mt("terminal", Ax);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Mx = [["path", {
    d: "M2 9a3 3 0 0 1 0 6v2a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-2a3 3 0 0 1 0-6V7a2 2 0 0 0-2-2H4a2 2 0 0 0-2 2Z",
    key: "qn84l0"
}], ["path", {
    d: "M13 5v2",
    key: "dyzc3o"
}], ["path", {
    d: "M13 17v2",
    key: "1ont0d"
}], ["path", {
    d: "M13 11v2",
    key: "1wjjxi"
}]]
  , Ox = Mt("ticket", Mx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const wx = [["path", {
    d: "M22 4s-.7 2.1-2 3.4c1.6 10-9.4 17.3-18 11.6 2.2.1 4.4-.6 6-2C3 15.5.5 9.6 3 5c2.2 2.6 5.6 4.1 9 4-.9-4.2 4-6.6 7-3.8 1.1 0 3-1.2 3-1.2z",
    key: "pff0z6"
}]]
  , pm = Mt("twitter", wx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Dx = [["path", {
    d: "M12 4v16",
    key: "1654pz"
}], ["path", {
    d: "M4 7V5a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v2",
    key: "e0r10z"
}], ["path", {
    d: "M9 20h6",
    key: "s66wpe"
}]]
  , Cx = Mt("type", Dx);
/**
 * @license lucide-react v0.554.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */
const Rx = [["path", {
    d: "M18 6 6 18",
    key: "1bl5f8"
}], ["path", {
    d: "m6 6 12 12",
    key: "d8bk6v"
}]]
  , Gm = Mt("x", Rx)
  , Ux = () => {
    const [s,d] = M.useState(!1)
      , [o,f] = M.useState(!1)
      , m = sl();
    M.useEffect( () => {
        const p = () => {
            f(window.scrollY > 50)
        }
        ;
        return window.addEventListener("scroll", p),
        () => window.removeEventListener("scroll", p)
    }
    , []),
    M.useEffect( () => {
        d(!1)
    }
    , [m]);
    const g = [{
        name: "الرئيسية",
        path: "/"
    }, {
        name: "الفعاليات",
        path: "/events"
    }, {
        name: "الجدول",
        path: "/calendar"
    }, {
        name: "القدية",
        path: "/qiddiya"
    }, {
        name: "عن المشروع",
        path: "/about"
    }, {
        name: "تواصل معنا",
        path: "/contact"
    }];
    return i.jsxs("nav", {
        className: `fixed top-0 w-full z-50 transition-all duration-300 ${o ? "bg-charcoal/95 backdrop-blur-md shadow-lg py-3" : "bg-transparent py-6"}`,
        children: [i.jsxs("div", {
            className: "container mx-auto px-6 flex justify-between items-center",
            children: [i.jsxs(Lt, {
                to: "/",
                className: "flex items-center space-x-2 space-x-reverse group",
                children: [i.jsx("div", {
                    className: "bg-gold w-10 h-10 rounded-lg flex items-center justify-center transform group-hover:rotate-45 transition-transform duration-300",
                    children: i.jsx(Lm, {
                        className: "text-charcoal w-6 h-6 fill-current group-hover:-rotate-45 transition-transform duration-300"
                    })
                }), i.jsxs("div", {
                    className: "text-white font-heading font-bold text-xl leading-none",
                    children: ["Visit", i.jsx("br", {}), i.jsx("span", {
                        className: "text-gold",
                        children: "Riyadh"
                    })]
                })]
            }), i.jsx("div", {
                className: "hidden md:flex items-center space-x-8 space-x-reverse",
                children: g.map(p => i.jsxs(Lt, {
                    to: p.path,
                    className: `text-sm font-bold font-body transition-colors duration-300 relative pb-1 group ${m.pathname === p.path ? "text-gold" : "text-white hover:text-gold"}`,
                    children: [p.name, i.jsx("span", {
                        className: `absolute bottom-0 right-0 h-0.5 bg-gold transition-all duration-300 ${m.pathname === p.path ? "w-full" : "w-0 group-hover:w-full"}`
                    })]
                }, p.path))
            }), i.jsx("button", {
                className: "md:hidden text-white hover:text-gold transition-colors",
                onClick: () => d(!s),
                children: s ? i.jsx(Gm, {
                    size: 28
                }) : i.jsx(px, {
                    size: 28
                })
            })]
        }), i.jsx("div", {
            className: `md:hidden fixed inset-0 bg-charcoal z-40 transition-transform duration-300 ease-in-out ${s ? "translate-x-0" : "translate-x-full"} pt-24 px-6`,
            children: i.jsx("div", {
                className: "flex flex-col space-y-6",
                children: g.map(p => i.jsx(Lt, {
                    to: p.path,
                    className: `text-2xl font-heading font-bold ${m.pathname === p.path ? "text-gold" : "text-white"}`,
                    children: p.name
                }, p.path))
            })
        })]
    })
}
  , Hx = () => i.jsx("footer", {
    className: "bg-black pt-16 pb-8 border-t border-gray-800",
    children: i.jsxs("div", {
        className: "container mx-auto px-6",
        children: [i.jsxs("div", {
            className: "grid grid-cols-1 md:grid-cols-4 gap-12 mb-12",
            children: [i.jsxs("div", {
                className: "col-span-1 md:col-span-1",
                children: [i.jsxs("div", {
                    className: "flex items-center space-x-2 space-x-reverse mb-6",
                    children: [i.jsx("div", {
                        className: "bg-gold w-8 h-8 rounded flex items-center justify-center",
                        children: i.jsx(Lm, {
                            className: "text-charcoal w-4 h-4 fill-current"
                        })
                    }), i.jsxs("h3", {
                        className: "text-xl font-bold font-heading text-white",
                        children: ["Visit ", i.jsx("span", {
                            className: "text-gold",
                            children: "Riyadh"
                        })]
                    })]
                }), i.jsx("p", {
                    className: "text-gray-400 text-sm leading-relaxed font-body",
                    children: "بوابتك الرقمية الأولى لاكتشاف روح العاصمة المتجددة. نقدم دليلاً عصرياً شاملاً لأرقى الفعاليات والمواسم الترفيهية في الرياض، مصمماً بمعايير عالمية ليواكب رؤية المملكة الطموحة.."
                })]
            }), i.jsxs("div", {
                children: [i.jsx("h4", {
                    className: "text-white font-bold font-heading mb-6",
                    children: "روابط سريعة"
                }), i.jsxs("ul", {
                    className: "space-y-3 text-sm text-gray-400 font-body",
                    children: [i.jsx("li", {
                        children: i.jsx(Lt, {
                            to: "/events",
                            className: "hover:text-gold transition-colors",
                            children: "جميع الفعاليات"
                        })
                    }), i.jsx("li", {
                        children: i.jsx(Lt, {
                            to: "/calendar",
                            className: "hover:text-gold transition-colors",
                            children: "جدول الأسبوع"
                        })
                    }), i.jsx("li", {
                        children: i.jsx(Lt, {
                            to: "/qiddiya",
                            className: "hover:text-gold transition-colors",
                            children: "مستقبل القدية"
                        })
                    }), i.jsx("li", {
                        children: i.jsx(Lt, {
                            to: "/about",
                            className: "hover:text-gold transition-colors",
                            children: "توثيق المشروع"
                        })
                    })]
                })]
            }), i.jsxs("div", {
                children: [i.jsx("h4", {
                    className: "text-white font-bold font-heading mb-6",
                    children: "تواصل معنا"
                }), i.jsxs("ul", {
                    className: "space-y-3 text-sm text-gray-400 font-body",
                    children: [i.jsxs("li", {
                        className: "flex items-center",
                        children: [i.jsx(xx, {
                            className: "w-4 h-4 ml-2 text-gold"
                        }), "contact@visitriyadh.sa"]
                    }), i.jsxs("li", {
                        className: "flex items-center",
                        children: [i.jsx(pm, {
                            className: "w-4 h-4 ml-2 text-gold"
                        }), "@VisitRiyadh"]
                    })]
                })]
            }), i.jsxs("div", {
                children: [i.jsx("h4", {
                    className: "text-white font-bold font-heading mb-6",
                    children: "النشرة البريدية"
                }), i.jsx("p", {
                    className: "text-gray-500 text-xs mb-4",
                    children: "اشترك لمعرفة آخر الأخبار"
                }), i.jsxs("div", {
                    className: "flex",
                    children: [i.jsx("input", {
                        type: "email",
                        placeholder: "بريدك الإلكتروني",
                        className: "bg-dark-gray text-white px-4 py-2 rounded-r-lg outline-none border border-gray-800 focus:border-gold w-full"
                    }), i.jsx("button", {
                        className: "bg-gold text-charcoal px-4 py-2 rounded-l-lg font-bold hover:bg-gold-light transition-colors",
                        children: "اشتراك"
                    })]
                })]
            })]
        }), i.jsxs("div", {
            className: "border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center",
            children: [i.jsx("p", {
                className: "text-gray-500 text-xs mb-4 md:mb-0",
                children: "© 2025 جميع الحقوق محفوظة - Visit Riyadh"
            }), i.jsxs("div", {
                className: "flex space-x-4 space-x-reverse",
                children: [i.jsx("a", {
                    href: "#",
                    className: "text-gray-400 hover:text-gold transition-colors",
                    children: i.jsx(rx, {
                        size: 20
                    })
                }), i.jsx("a", {
                    href: "#",
                    className: "text-gray-400 hover:text-gold transition-colors",
                    children: i.jsx(pm, {
                        size: 20
                    })
                }), i.jsx("a", {
                    href: "#",
                    className: "text-gray-400 hover:text-gold transition-colors",
                    children: i.jsx(hx, {
                        size: 20
                    })
                })]
            })]
        })]
    })
})
  , Ga = ({title: s, subtitle: d, center: o=!1, color: f="gold"}) => i.jsxs("div", {
    className: `mb-10 ${o ? "text-center" : "text-right"}`,
    children: [i.jsx("h2", {
        className: `text-3xl md:text-4xl font-bold font-heading mb-3 ${f === "gold" ? "text-gold" : "text-white"}`,
        children: s
    }), d && i.jsx("p", {
        className: "text-gray-400 text-lg font-body max-w-2xl mx-auto",
        children: d
    }), i.jsx("div", {
        className: `h-1 w-20 bg-gold mt-4 rounded-full ${o ? "mx-auto" : ""}`
    })]
})
  , Is = ({event: s, isOpen: d, onClose: o}) => {
    const f = Ks();
    if (!d || !s)
        return null;
    const m = () => {
        o(),
        f(`/events/${s.id}/order`)
    }
    ;
    return i.jsxs("div", {
        className: "fixed inset-0 z-[100] flex items-center justify-center p-4 animate-fade-in",
        children: [i.jsx("div", {
            className: "absolute inset-0 bg-black/80 backdrop-blur-sm",
            onClick: o
        }), i.jsxs("div", {
            className: "relative bg-white rounded-3xl overflow-hidden w-full max-w-lg shadow-2xl transform transition-all scale-100",
            children: [i.jsxs("div", {
                className: "relative h-56",
                children: [i.jsx("img", {
                    src: s.image,
                    alt: s.title,
                    className: "w-full h-full object-cover"
                }), i.jsx("div", {
                    className: "absolute inset-0 bg-gradient-to-t from-charcoal via-transparent to-transparent opacity-90"
                }), i.jsx("button", {
                    onClick: o,
                    className: "absolute top-4 right-4 bg-black/40 text-white p-2 rounded-full hover:bg-gold hover:text-charcoal transition-colors z-10 backdrop-blur-md",
                    children: i.jsx(Gm, {
                        size: 20
                    })
                }), i.jsxs("div", {
                    className: "absolute bottom-4 right-0 left-0 px-6 text-white text-right",
                    children: [i.jsx("span", {
                        className: "bg-gold text-charcoal text-xs font-bold px-3 py-1 rounded-full mb-2 inline-block",
                        children: s.type
                    }), i.jsx("h3", {
                        className: "text-2xl font-heading font-bold drop-shadow-md",
                        children: s.title
                    })]
                })]
            }), i.jsxs("div", {
                className: "p-8 text-right bg-white",
                children: [i.jsxs("div", {
                    className: "grid grid-cols-2 gap-4 mb-8",
                    children: [i.jsxs("div", {
                        className: "bg-soft-gray p-4 rounded-2xl flex flex-col items-end",
                        children: [i.jsxs("div", {
                            className: "flex items-center text-gray-400 mb-1",
                            children: [i.jsx("span", {
                                className: "text-xs font-bold mr-1",
                                children: "التاريخ"
                            }), i.jsx(gi, {
                                className: "w-4 h-4"
                            })]
                        }), i.jsx("span", {
                            className: "font-bold text-charcoal font-heading",
                            children: s.date
                        })]
                    }), i.jsxs("div", {
                        className: "bg-soft-gray p-4 rounded-2xl flex flex-col items-end",
                        children: [i.jsxs("div", {
                            className: "flex items-center text-gray-400 mb-1",
                            children: [i.jsx("span", {
                                className: "text-xs font-bold mr-1",
                                children: "الوقت"
                            }), i.jsx(Fs, {
                                className: "w-4 h-4"
                            })]
                        }), i.jsx("span", {
                            className: "font-bold text-charcoal font-heading",
                            children: s.time
                        })]
                    })]
                }), i.jsxs("div", {
                    className: "flex items-start justify-end mb-8",
                    children: [i.jsxs("div", {
                        className: "text-right mr-4",
                        children: [i.jsx("h4", {
                            className: "font-bold text-gray-400 text-xs mb-1 uppercase",
                            children: "الموقع"
                        }), i.jsx("p", {
                            className: "font-bold text-charcoal text-lg",
                            children: s.location
                        })]
                    }), i.jsx("div", {
                        className: "bg-gold/10 p-3 rounded-full shrink-0",
                        children: i.jsx(ta, {
                            className: "text-gold w-6 h-6"
                        })
                    })]
                }), i.jsxs("div", {
                    className: "bg-gray-50 border border-gray-100 rounded-2xl p-4 mb-8",
                    children: [i.jsxs("div", {
                        className: "flex justify-between items-center mb-2",
                        children: [i.jsx("span", {
                            className: "font-bold text-xl text-gold",
                            children: s.price || "150 ريال"
                        }), i.jsx("span", {
                            className: "text-gray-500 font-bold text-sm",
                            children: "سعر التذكرة"
                        })]
                    }), i.jsx("p", {
                        className: "text-gray-400 text-xs leading-relaxed",
                        children: "* السعر يشمل الضريبة ورسوم الخدمة. الأسعار قد تختلف حسب الفئة المختارة."
                    })]
                }), i.jsxs("button", {
                    onClick: m,
                    className: "w-full bg-charcoal text-white font-bold font-heading text-lg py-4 rounded-xl hover:bg-gold hover:text-charcoal transition-all shadow-xl hover:shadow-gold/20 flex items-center justify-center gap-2 group",
                    children: [i.jsx("span", {
                        children: "تأكيد الحجز والدفع"
                    }), i.jsx(La, {
                        className: "w-5 h-5 group-hover:scale-110 transition-transform"
                    })]
                })]
            })]
        })]
    })
}
  , oi = ({event: s}) => {
    const [d,o] = M.useState(!1);
    return i.jsxs(i.Fragment, {
        children: [i.jsxs("div", {
            className: "group relative bg-white rounded-2xl overflow-hidden shadow-lg transition-all duration-300 hover:-translate-y-2 hover:shadow-gold/20 hover:shadow-2xl flex flex-col h-full",
            children: [i.jsxs(Lt, {
                to: `/events/${s.id}`,
                className: "relative h-64 overflow-hidden shrink-0 block cursor-pointer",
                children: [i.jsx("img", {
                    src: s.image,
                    alt: s.title,
                    className: "w-full h-full object-cover transition-transform duration-500 group-hover:scale-110"
                }), i.jsx("div", {
                    className: "absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-60 group-hover:opacity-40 transition-opacity"
                }), i.jsx("span", {
                    className: "absolute top-4 right-4 bg-gold text-charcoal font-bold px-3 py-1 rounded-full text-sm font-body shadow-md",
                    children: s.type
                })]
            }), i.jsxs("div", {
                className: "p-6 relative flex flex-col flex-grow",
                children: [i.jsxs("div", {
                    className: "absolute -top-8 left-6 bg-white text-charcoal px-4 py-2 rounded-lg shadow-lg text-center min-w-[70px]",
                    children: [i.jsx("p", {
                        className: "text-sm font-bold text-gold",
                        children: s.time.split(" ")[0]
                    }), i.jsx("p", {
                        className: "text-xs font-bold text-gray-500",
                        children: s.time.split(" ")[1]
                    })]
                }), i.jsx(Lt, {
                    to: `/events/${s.id}`,
                    className: "block",
                    children: i.jsx("h3", {
                        className: "text-xl font-bold text-charcoal font-heading mb-2 group-hover:text-gold transition-colors line-clamp-1",
                        children: s.title
                    })
                }), i.jsx("p", {
                    className: "text-gray-600 text-sm font-body mb-4 line-clamp-2 h-10",
                    children: s.description
                }), i.jsxs("div", {
                    className: "flex flex-col space-y-2 text-sm text-gray-500 mb-6 font-body mt-auto",
                    children: [i.jsxs("div", {
                        className: "flex items-center",
                        children: [i.jsx(gi, {
                            className: "w-4 h-4 text-gold ml-2"
                        }), i.jsx("span", {
                            children: s.date
                        })]
                    }), i.jsxs("div", {
                        className: "flex items-center",
                        children: [i.jsx(ta, {
                            className: "w-4 h-4 text-gold ml-2"
                        }), i.jsx("span", {
                            children: s.location
                        })]
                    })]
                }), i.jsxs("button", {
                    onClick: () => o(!0),
                    className: "w-full py-3 rounded-xl border-2 border-charcoal text-charcoal font-bold font-body flex items-center justify-center group-hover:bg-charcoal group-hover:text-gold transition-all duration-300 cursor-pointer",
                    children: [i.jsx("span", {
                        children: "تفاصيل التذكرة"
                    }), i.jsx(Ym, {
                        className: "w-4 h-4 mr-2 transform group-hover:-translate-x-1 transition-transform"
                    })]
                })]
            })]
        }), i.jsx(Is, {
            event: s,
            isOpen: d,
            onClose: () => o(!1)
        })]
    })
}
;
var ue = (s => (s.Music = "موسيقى",
s.Theater = "مسرح",
s.Sports = "رياضة",
s.Family = "عائلي",
s.Dining = "مطاعم",
s.Exhibition = "معارض",
s))(ue || {});
const Ce = [{
    id: "101",
    title: "نور الرياض",
    description: "مهرجان سنوي يحتفي بفنون الضوء ويجمع فنانين محليين وعالميين في عروض ضوئية مبهرة تضيء سماء العاصمة.",
    image: "https://platinumlist.net/guide/wp-content/uploads/2024/09/Christopher-Bauder-AXION-2022.-Image-courtesy-the-artist.-Photo-%C2%A9-Noor-Riyadh-2022-a-Riyadh-Art-program-1.jpg",
    date: "2025-11-20",
    time: "06:00 م",
    location: "مركز الملك عبدالله المالي (KAFD)",
    type: ue.Exhibition,
    price: "مجاني",
    isTrending: !0,
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3623.5937905898863!2d46.64157777595357!3d24.765662149957367!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3e2ee32328452317%3A0x6a0669e256b823e5!2sKing%20Abdullah%20Financial%20District%20(KAFD)!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "102",
    title: "بوليفارد وورلد",
    description: "العالم بين يديك في تجربة ترفيهية متكاملة تجمع ثقافات 10 دول عالمية، مع أكبر بحيرة صناعية في العالم.",
    image: "https://images.unsplash.com/photo-1569930784237-ea65a2f40a83?q=80&w=1948&auto=format&fit=crop",
    date: "2025-11-20",
    time: "04:00 م",
    location: "بوليفارد وورلد",
    type: ue.Family,
    price: "يبدأ من 58 ريال",
    isTrending: !0,
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3622.754707421876!2d46.5986873!3d24.7695195!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3e2ee3e304918a23%3A0x8e83161c16543b5a!2sBoulevard%20World!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "103",
    title: "وندر جاردن",
    description: "حديقة ساحرة مليئة بالأشجار والأزهار النادرة والفراشات، مع ألعاب ترفيهية تناسب جميع أفراد العائلة.",
    image: "https://sadasaudi.net/wp-content/uploads/2024/11/1000_487519300a-scaled.webp",
    date: "2025-11-22",
    time: "04:00 م",
    location: "شمال الرياض",
    type: ue.Family,
    price: "يبدأ من 35 ريال",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d22957.618205897328!2d46.711533822259334!3d24.69640799836253!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjTCsDQ1JzM2LjQiTiA0NsKwMzknMTUuNiJF!5e0!3m2!1sen!2ssa!4v1654321234567!5m2!1sen!2ssa"
}, {
    id: "104",
    title: "معرض الرياض للسيارات",
    description: "أضخم تجمع للسيارات الكلاسيكية والفارهة والرياضية في الشرق الأوسط، يضم أندر الموديلات العالمية.",
    image: "https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?q=80&w=1966&auto=format&fit=crop",
    date: "2025-11-24",
    time: "05:00 م",
    location: "المملكة أرينا",
    type: ue.Exhibition,
    price: "يبدأ من 100 ريال",
    isTrending: !0,
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3622.793794123456!2d46.6025!3d24.7685!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3e2ee30000000001%3A0x123456789abcdef!2sKingdom%20Arena!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "105",
    title: "ساوند ستورم (MDLBEAST)",
    description: "أضخم مهرجان موسيقي في المنطقة، يجمع أكثر من 200 نجم عالمي ومحلي في تجربة صوتية وبصرية لا تضاهى.",
    image: "https://images.unsplash.com/photo-1598387993441-a364f854c3e1?q=80&w=2076&auto=format&fit=crop",
    date: "2025-12-12",
    time: "08:00 م",
    location: "بنبان",
    type: ue.Music,
    price: "يبدأ من 150 ريال",
    isTrending: !0,
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d57930.22272899169!2d46.5772!3d24.9658!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3e2efb7291079313%3A0x145555555555555!2sBanban!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "106",
    title: "كأس موسم الرياض للتنس",
    description: 'بطولة "Six Kings Slam" بمشاركة أساطير التنس العالميين في مواجهات نارية.',
    image: "https://rahhal.wego.com/wp-content/uploads/2023/10/riyadh-season-tennis-cup-featured.webp",
    date: "2025-12-05",
    time: "06:00 م",
    location: "ذا فينيو",
    type: ue.Sports,
    price: "يبدأ من 200 ريال",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3623!2d46.6!3d24.76!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zThe Venue!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "107",
    title: "ليب (LEAP 2025)",
    description: "المؤتمر التقني الأضخم عالمياً، حيث يلتقي قادة التكنولوجيا والمبتكرون لرسم ملامح المستقبل الرقمي. (منتهي)",
    image: "https://img.mstaml.com/i173799753455190018/%D9%85%D8%A4%D8%AA%D9%85%D8%B1-%D9%84%D9%8A%D8%A8-2025-%D8%A7%D9%83%D8%AA%D8%B4%D9%81-%D8%AC%D9%88%D8%A7%D8%A6%D8%B2-LEAP-2025-%D8%A7%D9%84%D9%86%D8%B3%D8%AE%D8%A9-%D8%A7%D9%84%D8%B1%D8%A7%D8%A8%D8%B9%D8%A9-%D8%A3%D9%83%D8%A8%D8%B1-%D8%AD%D8%AF%D8%AB-%D8%AA%D9%82%D9%86%D9%8A-%D9%81%D9%8A-%D8%A7%D9%84%D8%B3%D8%B9%D9%88%D8%AF%D9%8A%D8%A9-%D9%84%D9%8A%D8%A8-2025.webp",
    date: "2025-02-10",
    time: "10:00 ص",
    location: "مركز الرياض للمعارض والمؤتمرات",
    type: ue.Exhibition,
    price: "منتهي",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3621.565451234!2d46.7265!3d24.8145!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3e2eff63456789ab%3A0x123456789!2sRFECC!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "108",
    title: "كأس السعودية للفروسية",
    description: "أغلى سباق خيل في العالم، يجمع نخبة الجياد والفرسان في ميدان الملك عبدالعزيز للفروسية. (منتهي)",
    image: "https://jcsa.sa/globalassets/jcsa/images/saudi-cup-fixed/mbs_saudicup-12529.jpg",
    date: "2025-02-22",
    time: "03:00 م",
    location: "ميدان الملك عبدالعزيز",
    type: ue.Sports,
    price: "منتهي",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3618!2d46.8!3d24.9!2m3!1f0!2f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2sKing%20Abdulaziz%20Racetrack!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "109",
    title: "معرض الرياض للكتاب",
    description: "تظاهرة ثقافية كبرى تجمع دور النشر والمثقفين والقراء من جميع أنحاء العالم. (منتهي)",
    image: "https://images.unsplash.com/photo-1491841550275-ad7854e35ca6?q=80&w=1974&auto=format&fit=crop",
    date: "2025-10-05",
    time: "11:00 ص",
    location: "جامعة الملك سعود",
    type: ue.Exhibition,
    price: "مجاني",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3624!2d46.62!3d24.72!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2sKSU!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "110",
    title: "فورمولا إي الدرعية",
    description: "سباق السيارات الكهربائية الليلي في شوارع الدرعية التاريخية، يجمع بين التراث والمستقبل. (منتهي)",
    image: "https://images.unsplash.com/photo-1469854523086-cc02fe5d8800?q=80&w=2070&auto=format&fit=crop",
    date: "2025-01-26",
    time: "08:00 م",
    location: "الدرعية",
    type: ue.Sports,
    price: "منتهي",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3621!2d46.57!3d24.74!2m3!1f0!2f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2sDiriyah!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "111",
    title: "حفل جوائز Joy Awards",
    description: "أضخم حفل لتوزيع الجوائز الترفيهية في العالم العربي، بحضور نخبة من النجوم العالميين والعرب. (منتهي)",
    image: "https://images.unsplash.com/photo-1516450360452-9312f5e86fc7?q=80&w=2070&auto=format&fit=crop",
    date: "2025-01-18",
    time: "09:00 م",
    location: "مسرح بكر الشدي",
    type: ue.Music,
    price: "منتهي",
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3622!2d46.6!3d24.76!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2sBoulevard%20City!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}, {
    id: "112",
    title: "فيا رياض",
    description: "تجربة تسوق وتناول طعام فاخرة في واحدة من أرقى الوجهات في الرياض، بتصميم سلماني فريد.",
    image: "https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1974&auto=format&fit=crop",
    date: "2025-11-20",
    time: "07:00 م",
    location: "فيا رياض",
    type: ue.Dining,
    price: "حسب الطلب",
    isTrending: !0,
    mapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3624!2d46.65!3d24.68!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2sVia%20Riyadh!5e0!3m2!1sen!2ssa!4v1709564000000!5m2!1sen!2ssa"
}]
  , qx = [{
    id: "q1",
    title: "سيكس فلاجز القدية",
    description: "مدينة ملاهي عالمية ستحطم الأرقام القياسية بأسرع وأطول أفعوانية في العالم.",
    image: "https://images.unsplash.com/photo-1513883049090-d0b7439799bf?q=80&w=2070&auto=format&fit=crop"
}, {
    id: "q2",
    title: "مضمار السرعة",
    description: "حلبة سباق بمعايير F1 لاستضافة أكبر بطولات رياضة المحركات.",
    image: "https://images.unsplash.com/photo-1568605117036-5fe5e7bab0b7?q=80&w=2070&auto=format&fit=crop"
}, {
    id: "q3",
    title: "منطقة الفنون",
    description: "مسارح وقاعات حفلات مصممة بأحدث التقنيات لاستضافة الفعاليات العالمية.",
    image: "https://images.unsplash.com/photo-1549490349-8643362247b5?q=80&w=2070&auto=format&fit=crop"
}]
  , Bx = [{
    year: "2025",
    title: "الافتتاح الأولي",
    description: "افتتاح المرحلة الأولى وتشغيل المنتزهات الرئيسية."
}, {
    year: "2026",
    title: "مناطق جديدة",
    description: "توسع المناطق السكنية وافتتاح ملاعب الجولف."
}, {
    year: "2028",
    title: "التوسعات الكبرى",
    description: "اكتمال المجمع الرياضي والقرية الأولمبية."
}, {
    year: "2030",
    title: "التشغيل الكامل",
    description: "تحقيق الرؤية الكاملة واستقبال ملايين الزوار سنويًا."
}]
  , Yx = () => {
    const [s,d] = M.useState(0)
      , o = "2025-11-20"
      , f = N => N === o
      , m = N => N > o && N <= "2025-11-27"
      , g = N => N > "2025-11-27"
      , p = Ce.filter(N => f(N.date))
      , T = Ce.filter(N => m(N.date))
      , S = Ce.filter(N => g(N.date))
      , x = Ce.filter(N => N.isTrending);
    return M.useEffect( () => {
        const N = setInterval( () => {
            d(_ => (_ + 1) % x.length)
        }
        , 4e3);
        return () => clearInterval(N)
    }
    , [x.length]),
    i.jsxs("div", {
        className: "animate-fade-in",
        children: [i.jsxs("section", {
            className: "relative h-screen min-h-[600px] flex items-center justify-center overflow-hidden",
            children: [i.jsxs("div", {
                className: "absolute inset-0 z-0",
                children: [i.jsx("img", {
                    src: "https://images.unsplash.com/photo-1586724237569-f3d0c1dee8c6?q=80&w=2070&auto=format&fit=crop",
                    alt: "Visit Riyadh",
                    className: "w-full h-full object-cover"
                }), i.jsx("div", {
                    className: "absolute inset-0 bg-black/50"
                }), i.jsx("div", {
                    className: "absolute inset-0 bg-gradient-to-t from-black via-transparent to-black/30"
                })]
            }), i.jsxs("div", {
                className: "relative z-10 container mx-auto px-6 text-center",
                children: [i.jsxs("h1", {
                    className: "text-5xl md:text-7xl font-bold font-heading text-white mb-6 leading-tight drop-shadow-2xl",
                    children: ["فوق ", i.jsx("span", {
                        className: "text-gold",
                        children: "الخيال"
                    })]
                }), i.jsx("p", {
                    className: "text-xl md:text-2xl text-gray-200 font-body mb-4 max-w-3xl mx-auto font-light",
                    children: "دليلك الملهم لأبرز فعاليات الرياض. استكشف، خطط، واستمتع بلحظات لا تنسى."
                }), i.jsx("p", {
                    className: "text-3xl font-heading font-bold text-gold tracking-[0.3em] mb-10 drop-shadow-lg",
                    children: "KSA"
                }), i.jsxs("div", {
                    className: "flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-6 md:space-x-reverse",
                    children: [i.jsx(Lt, {
                        to: "/events",
                        className: "bg-gold text-charcoal font-bold text-lg px-10 py-4 rounded-full hover:bg-gold-light transition-all transform hover:scale-105 shadow-lg shadow-gold/20",
                        children: "اكتشف فعاليات اليوم"
                    }), i.jsx(Lt, {
                        to: "/qiddiya",
                        className: "bg-transparent border-2 border-white text-white font-bold text-lg px-10 py-4 rounded-full hover:bg-white hover:text-charcoal transition-all",
                        children: "مستقبل القدية"
                    })]
                })]
            }), i.jsxs("div", {
                className: "absolute bottom-10 w-full flex justify-center space-x-10 space-x-reverse text-white/70 text-sm font-body",
                children: [i.jsxs("div", {
                    className: "flex flex-col items-center",
                    children: [i.jsx("span", {
                        className: "font-bold text-gold text-lg",
                        children: "14"
                    }), i.jsx("span", {
                        children: "منطقة"
                    })]
                }), i.jsx("div", {
                    className: "h-10 w-px bg-white/20"
                }), i.jsxs("div", {
                    className: "flex flex-col items-center",
                    children: [i.jsx("span", {
                        className: "font-bold text-gold text-lg",
                        children: "+100"
                    }), i.jsx("span", {
                        children: "فعالية يومية"
                    })]
                }), i.jsx("div", {
                    className: "h-10 w-px bg-white/20"
                }), i.jsxs("div", {
                    className: "flex flex-col items-center",
                    children: [i.jsx("span", {
                        className: "font-bold text-gold text-lg",
                        children: "24/7"
                    }), i.jsx("span", {
                        children: "ترفيه مستمر"
                    })]
                })]
            })]
        }), i.jsx("section", {
            className: "py-20 bg-soft-gray text-charcoal",
            children: i.jsxs("div", {
                className: "container mx-auto px-6",
                children: [i.jsxs("div", {
                    className: "flex justify-between items-end mb-12",
                    children: [i.jsx(Ga, {
                        title: "فعاليات اليوم",
                        subtitle: "لا تفوت أبرز الأحداث المقامة حالياً في العاصمة",
                        color: "gold"
                    }), i.jsxs(Lt, {
                        to: "/calendar",
                        className: "hidden md:flex items-center text-gold font-bold hover:text-charcoal transition-colors mb-10",
                        children: ["عرض الجدول الكامل ", i.jsx(Ym, {
                            className: "w-4 h-4 mr-2"
                        })]
                    })]
                }), i.jsx("div", {
                    className: "grid grid-cols-1 md:grid-cols-3 gap-8",
                    children: p.length > 0 ? p.map(N => i.jsx(oi, {
                        event: N
                    }, N.id)) : i.jsx("div", {
                        className: "col-span-3 text-center py-10 text-gray-500",
                        children: "لا توجد فعاليات مسجلة لليوم"
                    })
                })]
            })
        }), i.jsx("section", {
            className: "py-20 bg-white text-charcoal border-t border-gray-100",
            children: i.jsxs("div", {
                className: "container mx-auto px-6",
                children: [i.jsx(Ga, {
                    title: "فعاليات الأسبوع",
                    subtitle: "خطط لعطلة نهاية الأسبوع وما بعدها",
                    color: "gold"
                }), i.jsxs("div", {
                    className: "grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-8",
                    children: [T.map(N => i.jsx(oi, {
                        event: N
                    }, N.id)), T.length === 0 && i.jsx("div", {
                        className: "col-span-full text-center py-10 text-gray-500",
                        children: "لا توجد فعاليات قادمة هذا الأسبوع"
                    })]
                })]
            })
        }), i.jsx("section", {
            className: "py-20 bg-soft-gray text-charcoal border-t border-gray-200",
            children: i.jsxs("div", {
                className: "container mx-auto px-6",
                children: [i.jsx(Ga, {
                    title: "فعاليات قادمة",
                    subtitle: "أبرز الفعاليات المنتظرة قريباً",
                    color: "gold"
                }), i.jsxs("div", {
                    className: "grid grid-cols-1 md:grid-cols-3 gap-8",
                    children: [S.map(N => i.jsx(oi, {
                        event: N
                    }, N.id)), S.length === 0 && i.jsx("div", {
                        className: "col-span-full text-center py-10 text-gray-500",
                        children: "سيتم الإعلان عن فعاليات الشهر قريباً"
                    })]
                })]
            })
        }), i.jsx("section", {
            className: "py-20 bg-charcoal overflow-hidden",
            children: i.jsxs("div", {
                className: "container mx-auto px-6",
                children: [i.jsx(Ga, {
                    title: "الأكثر رواجاً",
                    subtitle: "الفعاليات التي يتحدث عنها الجميع"
                }), i.jsxs("div", {
                    className: "relative h-[500px] w-full rounded-3xl overflow-hidden shadow-2xl border border-gray-800",
                    children: [x.map( (N, _) => i.jsxs("div", {
                        className: `absolute inset-0 transition-opacity duration-1000 ease-in-out ${_ === s ? "opacity-100 z-10" : "opacity-0 z-0"}`,
                        children: [i.jsx("img", {
                            src: N.image,
                            alt: N.title,
                            className: "w-full h-full object-cover"
                        }), i.jsx("div", {
                            className: "absolute inset-0 bg-gradient-to-r from-black via-black/50 to-transparent",
                            children: i.jsxs("div", {
                                className: "absolute bottom-0 right-0 p-10 md:p-20 max-w-2xl",
                                children: [i.jsx("span", {
                                    className: "bg-riyadh-purple text-white px-4 py-1 rounded-full text-sm font-bold mb-4 inline-block",
                                    children: N.type
                                }), i.jsx(Lt, {
                                    to: `/events/${N.id}`,
                                    children: i.jsx("h3", {
                                        className: "text-4xl md:text-5xl font-heading font-bold text-white mb-4 hover:text-gold transition-colors cursor-pointer",
                                        children: N.title
                                    })
                                }), i.jsx("p", {
                                    className: "text-gray-300 text-lg font-body mb-8 line-clamp-2",
                                    children: N.description
                                }), i.jsxs("div", {
                                    className: "flex space-x-6 space-x-reverse mb-8 text-gray-300",
                                    children: [i.jsxs("div", {
                                        className: "flex items-center",
                                        children: [i.jsx(gi, {
                                            className: "w-5 h-5 ml-2 text-gold"
                                        }), " ", N.date]
                                    }), i.jsxs("div", {
                                        className: "flex items-center",
                                        children: [i.jsx(ta, {
                                            className: "w-5 h-5 ml-2 text-gold"
                                        }), " ", N.location]
                                    })]
                                }), i.jsx(Lt, {
                                    to: `/events/${N.id}`,
                                    className: "bg-white text-charcoal font-bold px-8 py-3 rounded-lg hover:bg-gold transition-colors inline-block",
                                    children: "احجز تذكرتك الآن"
                                })]
                            })
                        })]
                    }, N.id)), i.jsx("div", {
                        className: "absolute bottom-6 left-1/2 transform -translate-x-1/2 z-20 flex space-x-2 space-x-reverse",
                        children: x.map( (N, _) => i.jsx("button", {
                            onClick: () => d(_),
                            className: `w-3 h-3 rounded-full transition-all duration-300 ${_ === s ? "bg-gold w-8" : "bg-white/50 hover:bg-white"}`
                        }, _))
                    })]
                })]
            })
        }), i.jsxs("section", {
            className: "py-24 bg-riyadh-purple relative overflow-hidden",
            children: [i.jsx("div", {
                className: "absolute top-0 right-0 w-64 h-64 bg-white/5 rounded-full blur-3xl -mr-20 -mt-20"
            }), i.jsx("div", {
                className: "absolute bottom-0 left-0 w-96 h-96 bg-night-blue/40 rounded-full blur-3xl -ml-20 -mb-20"
            }), i.jsxs("div", {
                className: "container mx-auto px-6 relative z-10 text-center",
                children: [i.jsxs("h2", {
                    className: "text-4xl md:text-6xl font-heading font-bold text-white mb-6",
                    children: ["مستقبل الترفيه.. ", i.jsx("br", {}), i.jsx("span", {
                        className: "text-gold",
                        children: "القدية"
                    })]
                }), i.jsx("p", {
                    className: "text-white/80 text-xl max-w-2xl mx-auto mb-10 font-light",
                    children: "مشاريع مستقبلية ستغير وجه الترفيه في العالم، تبدأ من قلب الرياض لتصل إلى عنان السماء."
                }), i.jsxs("div", {
                    className: "grid grid-cols-1 md:grid-cols-3 gap-6 mb-12",
                    children: [i.jsxs("div", {
                        className: "bg-white/10 backdrop-blur-sm p-6 rounded-2xl border border-white/10 hover:bg-white/20 transition-colors",
                        children: [i.jsx("h4", {
                            className: "text-xl font-bold text-gold mb-2",
                            children: "مدينة الألعاب"
                        }), i.jsx("p", {
                            className: "text-sm text-gray-300",
                            children: "الأكبر والأحدث في المنطقة"
                        })]
                    }), i.jsxs("div", {
                        className: "bg-white/10 backdrop-blur-sm p-6 rounded-2xl border border-white/10 hover:bg-white/20 transition-colors",
                        children: [i.jsx("h4", {
                            className: "text-xl font-bold text-gold mb-2",
                            children: "الاستاد الصخري"
                        }), i.jsx("p", {
                            className: "text-sm text-gray-300",
                            children: "تحفة معمارية فوق الجبال"
                        })]
                    }), i.jsxs("div", {
                        className: "bg-white/10 backdrop-blur-sm p-6 rounded-2xl border border-white/10 hover:bg-white/20 transition-colors",
                        children: [i.jsx("h4", {
                            className: "text-xl font-bold text-gold mb-2",
                            children: "مضمار السرعة"
                        }), i.jsx("p", {
                            className: "text-sm text-gray-300",
                            children: "موطن رياضة المحركات"
                        })]
                    })]
                }), i.jsx(Lt, {
                    to: "/qiddiya",
                    className: "inline-block bg-white text-riyadh-purple font-bold text-lg px-10 py-4 rounded-lg hover:shadow-xl transition-all transform hover:-translate-y-1",
                    children: "استكشف رؤية القدية"
                })]
            })]
        })]
    })
}
  , Lx = () => {
    const [s,d] = M.useState("")
      , [o,f] = M.useState("all")
      , [m,g] = M.useState("")
      , p = Ce.filter(T => {
        const S = T.title.includes(s) || T.location.includes(s)
          , x = o === "all" || T.type === o
          , N = m === "" || T.date === m;
        return S && x && N
    }
    );
    return Array.from(new Set(Ce.map(T => T.date))),
    i.jsxs("div", {
        className: "pt-24 pb-20 bg-dark-gray min-h-screen",
        children: [i.jsx("div", {
            className: "bg-charcoal py-16 mb-12 border-b border-gray-800",
            children: i.jsxs("div", {
                className: "container mx-auto px-6 text-center",
                children: [i.jsx("h1", {
                    className: "text-4xl md:text-5xl font-heading font-bold text-white mb-4",
                    children: "جميع الفعاليات"
                }), i.jsx("p", {
                    className: "text-gray-400 max-w-xl mx-auto",
                    children: "استعرض كافة الفعاليات المتاحة وقم بتصفيتها حسب رغبتك"
                })]
            })
        }), i.jsxs("div", {
            className: "container mx-auto px-6",
            children: [i.jsx("div", {
                className: "bg-white rounded-2xl p-6 shadow-xl mb-12 -mt-24 relative z-10",
                children: i.jsxs("div", {
                    className: "grid grid-cols-1 md:grid-cols-4 gap-4",
                    children: [i.jsxs("div", {
                        className: "relative col-span-1 md:col-span-1",
                        children: [i.jsx(jx, {
                            className: "absolute top-1/2 right-3 transform -translate-y-1/2 text-gray-400 w-5 h-5"
                        }), i.jsx("input", {
                            type: "text",
                            placeholder: "ابحث عن فعالية أو موقع...",
                            className: "w-full bg-soft-gray text-charcoal pl-4 pr-10 py-3 rounded-lg focus:outline-none focus:ring-2 focus:ring-gold transition-all",
                            value: s,
                            onChange: T => d(T.target.value)
                        })]
                    }), i.jsxs("div", {
                        className: "relative",
                        children: [i.jsx(sx, {
                            className: "absolute top-1/2 right-3 transform -translate-y-1/2 text-gray-400 w-5 h-5 pointer-events-none"
                        }), i.jsxs("select", {
                            className: "w-full bg-soft-gray text-charcoal pl-4 pr-10 py-3 rounded-lg focus:outline-none focus:ring-2 focus:ring-gold appearance-none cursor-pointer",
                            value: o,
                            onChange: T => f(T.target.value),
                            children: [i.jsx("option", {
                                value: "all",
                                children: "جميع التصنيفات"
                            }), Object.values(ue).map(T => i.jsx("option", {
                                value: T,
                                children: T
                            }, T))]
                        })]
                    }), i.jsx("div", {
                        className: "relative",
                        children: i.jsx("input", {
                            type: "date",
                            className: "w-full bg-soft-gray text-charcoal px-4 py-3 rounded-lg focus:outline-none focus:ring-2 focus:ring-gold cursor-pointer",
                            value: m,
                            onChange: T => g(T.target.value)
                        })
                    }), i.jsx("button", {
                        onClick: () => {
                            d(""),
                            f("all"),
                            g("")
                        }
                        ,
                        className: "bg-charcoal text-white font-bold rounded-lg hover:bg-gold hover:text-charcoal transition-colors",
                        children: "إعادة تعيين"
                    })]
                })
            }), i.jsxs("div", {
                className: "mb-8 text-gray-400 text-sm",
                children: ["تم العثور على ", p.length, " فعالية"]
            }), p.length > 0 ? i.jsx("div", {
                className: "grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8",
                children: p.map(T => i.jsx(oi, {
                    event: T
                }, T.id))
            }) : i.jsxs("div", {
                className: "text-center py-20",
                children: [i.jsx("div", {
                    className: "text-6xl mb-4",
                    children: "🔍"
                }), i.jsx("h3", {
                    className: "text-2xl font-bold text-white mb-2",
                    children: "لا توجد نتائج"
                }), i.jsx("p", {
                    className: "text-gray-500",
                    children: "جرب تغيير خيارات البحث أو الفلترة"
                })]
            })]
        })]
    })
}
  , Gx = () => {
    const [s,d] = M.useState("day")
      , [o,f] = M.useState(0)
      , [m,g] = M.useState("2025-11-20")
      , [p,T] = M.useState(null)
      , S = "2025-11-20"
      , x = Ce.filter(U => U.date === S)
      , N = ["السبت", "الأحد", "الإثنين", "الثلاثاء", "الأربعاء", "الخميس", "الجمعة"]
      , _ = Array.from({
        length: 30
    }, (U, L) => L + 1)
      , H = Ce.filter(U => U.date === m);
    return i.jsxs("div", {
        className: "pt-24 pb-20 bg-charcoal min-h-screen",
        children: [i.jsxs("div", {
            className: "container mx-auto px-6",
            children: [i.jsx(Ga, {
                title: "جدول الفعاليات",
                subtitle: "نظم وقتك واستمتع بكل لحظة"
            }), i.jsx("div", {
                className: "flex justify-center mb-12",
                children: i.jsxs("div", {
                    className: "bg-dark-gray p-1 rounded-xl inline-flex flex-wrap justify-center shadow-inner",
                    children: [i.jsx("button", {
                        onClick: () => d("day"),
                        className: `px-6 md:px-8 py-3 rounded-lg font-bold text-sm transition-all ${s === "day" ? "bg-gold text-charcoal shadow-lg transform scale-105" : "text-gray-400 hover:text-white"}`,
                        children: "جدول اليوم"
                    }), i.jsx("button", {
                        onClick: () => d("week"),
                        className: `px-6 md:px-8 py-3 rounded-lg font-bold text-sm transition-all ${s === "week" ? "bg-gold text-charcoal shadow-lg transform scale-105" : "text-gray-400 hover:text-white"}`,
                        children: "جدول الأسبوع"
                    }), i.jsx("button", {
                        onClick: () => d("month"),
                        className: `px-6 md:px-8 py-3 rounded-lg font-bold text-sm transition-all ${s === "month" ? "bg-gold text-charcoal shadow-lg transform scale-105" : "text-gray-400 hover:text-white"}`,
                        children: "جدول الشهر"
                    })]
                })
            }), s === "day" && i.jsxs("div", {
                className: "bg-white rounded-3xl overflow-hidden shadow-2xl animate-fade-in",
                children: [i.jsxs("div", {
                    className: "bg-gray-100 px-8 py-4 border-b border-gray-200 flex justify-between items-center",
                    children: [i.jsx("span", {
                        className: "text-charcoal font-bold font-heading text-lg",
                        children: "اليوم، 20 نوفمبر"
                    }), i.jsxs("span", {
                        className: "text-gold font-bold bg-charcoal px-3 py-1 rounded-full text-xs",
                        children: [x.length, " فعاليات"]
                    })]
                }), i.jsxs("div", {
                    className: "divide-y divide-gray-100",
                    children: [x.map(U => i.jsxs("div", {
                        className: "p-6 hover:bg-gray-50 transition-colors flex flex-col md:flex-row items-center md:justify-between gap-6",
                        children: [i.jsxs("div", {
                            className: "flex items-center w-full md:w-auto text-right md:text-right",
                            children: [i.jsxs("div", {
                                className: "text-center px-4 pl-6 border-l border-gray-200 ml-6 hidden md:block",
                                children: [i.jsx("span", {
                                    className: "block text-xl font-bold text-charcoal",
                                    children: U.time.split(" ")[0]
                                }), i.jsx("span", {
                                    className: "block text-xs text-gray-500",
                                    children: U.time.split(" ")[1]
                                })]
                            }), i.jsxs("div", {
                                children: [i.jsx("h4", {
                                    className: "text-lg font-bold text-charcoal mb-1",
                                    children: U.title
                                }), i.jsxs("div", {
                                    className: "flex items-center text-gray-500 text-sm",
                                    children: [i.jsx(ta, {
                                        className: "w-3 h-3 ml-1"
                                    }), " ", U.location]
                                }), i.jsx("div", {
                                    className: "md:hidden mt-2 text-xs font-bold text-gold",
                                    children: U.time
                                })]
                            })]
                        }), i.jsxs("div", {
                            className: "flex items-center gap-4 w-full md:w-auto justify-between md:justify-end",
                            children: [i.jsx("span", {
                                className: "bg-gray-200 text-gray-700 px-3 py-1 rounded text-sm",
                                children: U.type
                            }), i.jsx("button", {
                                onClick: () => T(U),
                                className: "text-gold font-bold border border-gold px-6 py-2 rounded hover:bg-gold hover:text-white transition-colors text-sm shadow-sm",
                                children: "حجز"
                            })]
                        })]
                    }, U.id)), x.length === 0 && i.jsx("div", {
                        className: "p-10 text-center text-gray-500",
                        children: "لا توجد فعاليات مسجلة لهذا اليوم."
                    })]
                })]
            }), s === "week" && i.jsxs("div", {
                className: "animate-fade-in",
                children: [i.jsx("div", {
                    className: "grid grid-cols-4 md:grid-cols-7 gap-2 mb-8",
                    children: N.map( (U, L) => i.jsxs("button", {
                        onClick: () => f(L),
                        className: `py-4 rounded-xl text-center transition-all ${o === L ? "bg-gold text-charcoal font-bold transform -translate-y-2 shadow-lg" : "bg-dark-gray text-gray-400 hover:bg-gray-800"}`,
                        children: [i.jsx("span", {
                            className: "block text-sm mb-1",
                            children: U
                        }), i.jsx("span", {
                            className: "block text-lg font-heading font-bold",
                            children: 20 + L
                        })]
                    }, L))
                }), i.jsxs("div", {
                    className: "bg-dark-gray p-8 rounded-3xl text-center border border-gray-800 min-h-[300px]",
                    children: [i.jsxs("p", {
                        className: "text-gray-400 mb-6",
                        children: ["فعاليات يوم ", N[o], " الموافق ", 20 + o, " نوفمبر"]
                    }), i.jsx("div", {
                        className: "grid grid-cols-1 md:grid-cols-2 gap-4",
                        children: Ce.slice(0, o % 3 + 2).map(U => i.jsxs("div", {
                            className: "bg-charcoal p-4 rounded-xl flex items-center text-right border border-gray-700 hover:border-gold transition-colors cursor-pointer group relative overflow-hidden",
                            children: [i.jsx("img", {
                                src: U.image,
                                className: "w-16 h-16 rounded-lg object-cover ml-4 group-hover:scale-105 transition-transform",
                                alt: U.title
                            }), i.jsxs("div", {
                                className: "flex-grow",
                                children: [i.jsx("h5", {
                                    className: "text-white font-bold mb-1 group-hover:text-gold transition-colors",
                                    children: U.title
                                }), i.jsxs("p", {
                                    className: "text-xs text-gray-500",
                                    children: [U.time, " | ", U.location]
                                })]
                            }), i.jsx("button", {
                                onClick: () => T(U),
                                className: "text-xs bg-gold text-charcoal px-3 py-1 rounded opacity-0 group-hover:opacity-100 transition-opacity font-bold absolute left-4 bottom-4 md:static md:opacity-100",
                                children: "حجز"
                            })]
                        }, U.id))
                    })]
                })]
            }), s === "month" && i.jsxs("div", {
                className: "animate-fade-in",
                children: [i.jsxs("div", {
                    className: "bg-white rounded-3xl p-8 shadow-2xl mb-8",
                    children: [i.jsxs("div", {
                        className: "flex justify-between items-center mb-6",
                        children: [i.jsx("h3", {
                            className: "text-2xl font-bold font-heading text-charcoal",
                            children: "نوفمبر 2025"
                        }), i.jsxs("div", {
                            className: "flex items-center gap-2 text-sm text-gray-500",
                            children: [i.jsx("span", {
                                className: "w-2 h-2 bg-gold rounded-full"
                            }), i.jsx("span", {
                                children: "يوجد فعالية"
                            })]
                        })]
                    }), i.jsx("div", {
                        className: "grid grid-cols-7 gap-2 mb-2 text-center font-bold text-gray-400 text-sm",
                        children: N.map(U => i.jsx("div", {
                            children: U
                        }, U))
                    }), i.jsx("div", {
                        className: "grid grid-cols-7 gap-2",
                        children: _.map(U => {
                            const L = `2025-11-${U.toString().padStart(2, "0")}`
                              , J = Ce.some(Z => Z.date === L)
                              , X = m === L;
                            return i.jsxs("button", {
                                onClick: () => g(L),
                                className: `
                          relative min-h-[60px] md:min-h-[100px] rounded-xl flex flex-col items-center justify-center border transition-all duration-200
                          ${X ? "bg-charcoal text-white border-charcoal shadow-lg transform scale-105 z-10" : "bg-soft-gray text-charcoal border-gray-100 hover:border-gold hover:bg-white"}
                        `,
                                children: [i.jsx("span", {
                                    className: `text-lg md:text-2xl font-bold font-heading ${X ? "text-gold" : ""}`,
                                    children: U
                                }), J && i.jsx("span", {
                                    className: `absolute bottom-2 w-2 h-2 rounded-full ${X ? "bg-white" : "bg-gold animate-pulse"}`
                                })]
                            }, U)
                        }
                        )
                    })]
                }), i.jsxs("div", {
                    className: "bg-dark-gray p-8 rounded-3xl border border-gray-800 transition-all",
                    children: [i.jsxs("div", {
                        className: "flex items-center justify-between mb-6",
                        children: [i.jsxs("h4", {
                            className: "text-white font-bold text-xl flex items-center",
                            children: ["فعاليات ", m]
                        }), i.jsx("span", {
                            className: "bg-gold text-charcoal font-bold text-sm px-3 py-1 rounded-full",
                            children: H.length
                        })]
                    }), H.length > 0 ? i.jsx("div", {
                        className: "grid grid-cols-1 md:grid-cols-2 gap-4",
                        children: H.map(U => i.jsxs("div", {
                            className: "bg-charcoal p-4 rounded-xl flex items-center text-right border border-gray-700 hover:border-gold transition-colors group",
                            children: [i.jsx("img", {
                                src: U.image,
                                className: "w-20 h-20 rounded-lg object-cover ml-4 group-hover:scale-105 transition-transform",
                                alt: U.title
                            }), i.jsxs("div", {
                                className: "flex-grow",
                                children: [i.jsxs("div", {
                                    className: "flex justify-between items-start",
                                    children: [i.jsx("h5", {
                                        className: "text-white font-bold mb-1 group-hover:text-gold transition-colors",
                                        children: U.title
                                    }), i.jsx("span", {
                                        className: "bg-white/10 text-xs text-white px-2 py-1 rounded mb-1 inline-block",
                                        children: U.type
                                    })]
                                }), i.jsxs("div", {
                                    className: "text-xs text-gray-500 space-y-1",
                                    children: [i.jsxs("p", {
                                        className: "flex items-center gap-2",
                                        children: [i.jsx(Fs, {
                                            size: 12,
                                            className: "text-gold"
                                        }), " ", U.time]
                                    }), i.jsxs("p", {
                                        className: "flex items-center gap-2",
                                        children: [i.jsx(ta, {
                                            size: 12,
                                            className: "text-gold"
                                        }), " ", U.location]
                                    })]
                                })]
                            }), i.jsx("button", {
                                onClick: () => T(U),
                                className: "mr-4 bg-gold text-charcoal text-sm font-bold px-4 py-2 rounded hover:bg-white transition-colors",
                                children: "حجز"
                            })]
                        }, U.id))
                    }) : i.jsxs("div", {
                        className: "text-center py-10 bg-charcoal/50 rounded-xl border border-dashed border-gray-700",
                        children: [i.jsx("p", {
                            className: "text-gray-500 mb-2",
                            children: "لا توجد فعاليات مسجلة في هذا التاريخ"
                        }), i.jsx("p", {
                            className: "text-sm text-gray-600",
                            children: "جرب اختيار يوم آخر مميز بنقطة ذهبية"
                        })]
                    })]
                })]
            })]
        }), i.jsx(Is, {
            event: p,
            isOpen: !!p,
            onClose: () => T(null)
        })]
    })
}
  , Xx = () => i.jsxs("div", {
    className: "bg-black text-white overflow-hidden",
    children: [i.jsxs("div", {
        className: "relative h-screen flex items-center justify-center",
        children: [i.jsxs("div", {
            className: "absolute inset-0",
            children: [i.jsx("img", {
                src: "https://picsum.photos/id/1033/1920/1080",
                alt: "Qiddiya Future",
                className: "w-full h-full object-cover opacity-60"
            }), i.jsx("div", {
                className: "absolute inset-0 bg-gradient-to-b from-black/30 via-transparent to-black"
            })]
        }), i.jsxs("div", {
            className: "relative z-10 text-center px-6",
            children: [i.jsx("h1", {
                className: "text-6xl md:text-8xl font-heading font-extrabold mb-4 tracking-tight text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-blue-500",
                children: "القدية"
            }), i.jsx("p", {
                className: "text-2xl md:text-3xl font-light text-gray-200 max-w-3xl mx-auto",
                children: "عاصمة الترفيه والرياضة والفنون في المستقبل"
            })]
        }), i.jsx("div", {
            className: "absolute bottom-10 left-0 right-0 text-center animate-bounce",
            children: i.jsx("span", {
                className: "text-gray-400 text-sm",
                children: "اكتشف المزيد"
            })
        })]
    }), i.jsxs("section", {
        className: "py-24 container mx-auto px-6",
        children: [i.jsxs("h2", {
            className: "text-4xl font-heading font-bold mb-16 text-center",
            children: ["مناطق ", i.jsx("span", {
                className: "text-riyadh-purple",
                children: "المستقبل"
            })]
        }), i.jsx("div", {
            className: "grid grid-cols-1 gap-20",
            children: qx.map( (s, d) => i.jsxs("div", {
                className: `flex flex-col md:flex-row items-center gap-10 ${d % 2 !== 0 ? "md:flex-row-reverse" : ""}`,
                children: [i.jsx("div", {
                    className: "w-full md:w-1/2",
                    children: i.jsxs("div", {
                        className: "relative rounded-3xl overflow-hidden group",
                        children: [i.jsx("img", {
                            src: s.image,
                            alt: s.title,
                            className: "w-full h-80 object-cover transform group-hover:scale-110 transition-transform duration-700"
                        }), i.jsx("div", {
                            className: "absolute inset-0 bg-riyadh-purple/20 group-hover:bg-transparent transition-colors"
                        })]
                    })
                }), i.jsxs("div", {
                    className: "w-full md:w-1/2 text-right",
                    children: [i.jsx("h3", {
                        className: "text-3xl font-bold mb-4 text-white",
                        children: s.title
                    }), i.jsx("p", {
                        className: "text-gray-400 text-lg leading-relaxed mb-6",
                        children: s.description
                    }), i.jsx("button", {
                        className: "text-riyadh-purple font-bold border-b border-riyadh-purple pb-1 hover:text-white hover:border-white transition-all",
                        children: "عرض التفاصيل والمخططات"
                    })]
                })]
            }, s.id))
        })]
    }), i.jsx("section", {
        className: "py-24 bg-dark-gray relative",
        children: i.jsxs("div", {
            className: "container mx-auto px-6",
            children: [i.jsx("h2", {
                className: "text-4xl font-heading font-bold mb-16 text-center text-gold",
                children: "الجدول الزمني للمشروع"
            }), i.jsxs("div", {
                className: "relative",
                children: [i.jsx("div", {
                    className: "absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-gray-800 hidden md:block"
                }), i.jsx("div", {
                    className: "space-y-12",
                    children: Bx.map( (s, d) => i.jsxs("div", {
                        className: `flex flex-col md:flex-row items-center justify-between relative ${d % 2 === 0 ? "md:flex-row-reverse" : ""}`,
                        children: [i.jsx("div", {
                            className: "w-full md:w-5/12"
                        }), i.jsx("div", {
                            className: "z-10 bg-charcoal border-4 border-gold rounded-full w-16 h-16 flex items-center justify-center font-bold text-white shadow-lg mb-4 md:mb-0",
                            children: s.year
                        }), i.jsxs("div", {
                            className: `w-full md:w-5/12 bg-charcoal p-8 rounded-2xl border border-gray-800 hover:border-gold transition-colors ${d % 2 === 0 ? "text-right" : "text-right md:text-left"}`,
                            children: [i.jsx("h4", {
                                className: "text-xl font-bold text-white mb-2",
                                children: s.title
                            }), i.jsx("p", {
                                className: "text-gray-400",
                                children: s.description
                            })]
                        })]
                    }, d))
                })]
            })]
        })
    })]
})
  , Qx = () => i.jsx("div", {
    className: "pt-24 pb-20 bg-charcoal min-h-screen",
    children: i.jsx("div", {
        className: "container mx-auto px-6",
        children: i.jsxs("div", {
            className: "bg-white rounded-3xl p-8 md:p-12 shadow-xl mb-10 overflow-hidden relative",
            children: [i.jsx("div", {
                className: "absolute top-0 left-0 w-full h-2 bg-gradient-to-r from-gold to-riyadh-purple"
            }), i.jsx("div", {
                className: "absolute -bottom-20 -left-20 w-64 h-64 bg-gold/5 rounded-full blur-3xl"
            }), i.jsxs("div", {
                className: "max-w-5xl mx-auto text-right relative z-10",
                children: [i.jsxs("div", {
                    className: "text-center mb-12",
                    children: [i.jsxs("h1", {
                        className: "text-3xl md:text-5xl font-heading font-bold text-charcoal mb-4",
                        children: ["🌟 حول مشروع: ", i.jsx("span", {
                            className: "text-gold",
                            children: "Visit Riyadh"
                        })]
                    }), i.jsx("p", {
                        className: "text-xl text-gray-500 font-body",
                        children: "دليلك للفعاليات والترفيه في قلب العاصمة"
                    })]
                }), i.jsxs("div", {
                    className: "space-y-16 font-body text-lg leading-relaxed",
                    children: [i.jsxs("div", {
                        className: "flex flex-col md:flex-row gap-10 items-start",
                        children: [i.jsxs("div", {
                            className: "w-full md:w-2/3",
                            children: [i.jsxs("h3", {
                                className: "text-2xl font-bold font-heading mb-6 text-charcoal flex items-center gap-2",
                                children: [i.jsx("span", {
                                    className: "text-2xl",
                                    children: "💡"
                                }), " نظرة عامة ورؤية المشروع"]
                            }), i.jsxs("div", {
                                className: "text-gray-600 space-y-4",
                                children: [i.jsxs("p", {
                                    children: ["تم تطوير هذا المشروع كجزء من متطلبات التخرج، بجهود الطالب ", i.jsx("span", {
                                        className: "text-charcoal font-bold",
                                        children: "خالد"
                                    }), "، بهدف إنشاء منصة ويب عصرية ومبتكرة. المنصة هي الدليل المتكامل لزوار فعاليات ومهرجانات مدينة الرياض، وتهدف لتقديم تجربة تصفح سريعة وجذابة تعكس المستوى الفاخر للفعاليات التي تستضيفها المملكة."]
                                }), i.jsx("p", {
                                    children: "المشروع ليس مجرد موقع لعرض البيانات، بل هو واجهة مستخدم (UI) متطورة تم تصميمها لتوفير تجربة مستخدم (UX) سلسة، مع التركيز على الهوية البصرية التي تتماشى مع رؤية المملكة الترفيهية."
                                })]
                            })]
                        }), i.jsxs("div", {
                            className: "w-full md:w-1/3 bg-gray-50 p-6 rounded-2xl border border-gray-100 shadow-sm",
                            children: [i.jsx("h4", {
                                className: "font-bold text-gold mb-4 text-center",
                                children: "أبرز المميزات"
                            }), i.jsxs("ul", {
                                className: "space-y-3 text-sm text-gray-600",
                                children: [i.jsxs("li", {
                                    className: "flex items-center gap-2",
                                    children: [i.jsx(La, {
                                        className: "w-4 h-4 text-green-500"
                                    }), " تصميم عصري وجذاب"]
                                }), i.jsxs("li", {
                                    className: "flex items-center gap-2",
                                    children: [i.jsx(La, {
                                        className: "w-4 h-4 text-green-500"
                                    }), " تجربة مستخدم سلسة"]
                                }), i.jsxs("li", {
                                    className: "flex items-center gap-2",
                                    children: [i.jsx(La, {
                                        className: "w-4 h-4 text-green-500"
                                    }), " أداء عالي وسريع"]
                                }), i.jsxs("li", {
                                    className: "flex items-center gap-2",
                                    children: [i.jsx(La, {
                                        className: "w-4 h-4 text-green-500"
                                    }), " هوية بصرية فاخرة"]
                                })]
                            })]
                        })]
                    }), i.jsxs("div", {
                        children: [i.jsxs("h3", {
                            className: "text-2xl font-bold font-heading mb-8 text-charcoal flex items-center gap-2",
                            children: [i.jsx("span", {
                                className: "text-2xl",
                                children: "🛠️"
                            }), " الأدوات والتقنيات الأساسية المستخدمة"]
                        }), i.jsx("p", {
                            className: "text-gray-600 mb-8 max-w-3xl",
                            children: "تم بناء هذا المشروع على أحدث التقنيات لضمان الأداء العالي والقابلية للتوسع، بالاعتماد على المكدس التقني التالي:"
                        }), i.jsxs("div", {
                            className: "grid grid-cols-1 md:grid-cols-2 gap-6",
                            children: [i.jsxs("div", {
                                className: "bg-gray-50 hover:bg-white hover:shadow-lg transition-all p-6 rounded-2xl border border-gray-200 flex items-start gap-4",
                                children: [i.jsx("div", {
                                    className: "bg-blue-100 p-3 rounded-lg text-blue-600 shrink-0",
                                    children: i.jsx(ix, {
                                        size: 24
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("h4", {
                                        className: "font-bold text-lg text-charcoal mb-1",
                                        children: "React 18"
                                    }), i.jsx("p", {
                                        className: "text-sm text-gray-500 font-bold mb-1",
                                        children: "واجهة المستخدم (Frontend)"
                                    }), i.jsx("p", {
                                        className: "text-gray-600 text-sm",
                                        children: "المكتبة الأساسية لبناء واجهة المستخدم التفاعلية ذات المكونات (Component-Based)."
                                    })]
                                })]
                            }), i.jsxs("div", {
                                className: "bg-gray-50 hover:bg-white hover:shadow-lg transition-all p-6 rounded-2xl border border-gray-200 flex items-start gap-4",
                                children: [i.jsx("div", {
                                    className: "bg-blue-100 p-3 rounded-lg text-blue-800 shrink-0",
                                    children: i.jsx(_x, {
                                        size: 24
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("h4", {
                                        className: "font-bold text-lg text-charcoal mb-1",
                                        children: "TypeScript"
                                    }), i.jsx("p", {
                                        className: "text-sm text-gray-500 font-bold mb-1",
                                        children: "لغة البرمجة"
                                    }), i.jsx("p", {
                                        className: "text-gray-600 text-sm",
                                        children: "استخدام لغة مبرمجة لضمان جودة الكود وتجنب الأخطاء البرمجية قبل التشغيل."
                                    })]
                                })]
                            }), i.jsxs("div", {
                                className: "bg-gray-50 hover:bg-white hover:shadow-lg transition-all p-6 rounded-2xl border border-gray-200 flex items-start gap-4",
                                children: [i.jsx("div", {
                                    className: "bg-teal-100 p-3 rounded-lg text-teal-600 shrink-0",
                                    children: i.jsx(Sx, {
                                        size: 24
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("h4", {
                                        className: "font-bold text-lg text-charcoal mb-1",
                                        children: "Tailwind CSS"
                                    }), i.jsx("p", {
                                        className: "text-sm text-gray-500 font-bold mb-1",
                                        children: "التصميم والستايل"
                                    }), i.jsx("p", {
                                        className: "text-gray-600 text-sm",
                                        children: "إطار عمل لبناء التصميمات بسرعة ومرونة عالية، مما يضمن استجابة الموقع لجميع الأجهزة."
                                    })]
                                })]
                            }), i.jsxs("div", {
                                className: "bg-gray-50 hover:bg-white hover:shadow-lg transition-all p-6 rounded-2xl border border-gray-200 flex items-start gap-4",
                                children: [i.jsx("div", {
                                    className: "bg-orange-100 p-3 rounded-lg text-orange-600 shrink-0",
                                    children: i.jsx(Cx, {
                                        size: 24
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("h4", {
                                        className: "font-bold text-lg text-charcoal mb-1",
                                        children: "Google Fonts"
                                    }), i.jsx("p", {
                                        className: "text-sm text-gray-500 font-bold mb-1",
                                        children: "الخطوط"
                                    }), i.jsx("p", {
                                        className: "text-gray-600 text-sm",
                                        children: "استخدام خطوط احترافية لتعزيز الهوية البصرية وقراءة المحتوى."
                                    })]
                                })]
                            })]
                        })]
                    })]
                })]
            })]
        })
    })
})
  , Zx = () => i.jsx("div", {
    className: "pt-24 pb-20 bg-charcoal min-h-screen flex items-center",
    children: i.jsx("div", {
        className: "container mx-auto px-6",
        children: i.jsxs("div", {
            className: "max-w-2xl mx-auto bg-dark-gray p-8 md:p-12 rounded-3xl shadow-2xl border border-gray-800",
            children: [i.jsx(Ga, {
                title: "تواصل معنا",
                subtitle: "نحن هنا للإجابة على استفساراتك",
                center: !0
            }), i.jsxs("form", {
                className: "space-y-6",
                onSubmit: s => s.preventDefault(),
                children: [i.jsxs("div", {
                    children: [i.jsx("label", {
                        className: "block text-gray-400 mb-2 font-bold",
                        children: "الاسم الكامل"
                    }), i.jsx("input", {
                        type: "text",
                        className: "w-full bg-charcoal text-white border border-gray-700 rounded-lg px-4 py-3 focus:border-gold focus:ring-1 focus:ring-gold outline-none transition-colors",
                        placeholder: "أدخل اسمك"
                    })]
                }), i.jsxs("div", {
                    children: [i.jsx("label", {
                        className: "block text-gray-400 mb-2 font-bold",
                        children: "البريد الإلكتروني"
                    }), i.jsx("input", {
                        type: "email",
                        className: "w-full bg-charcoal text-white border border-gray-700 rounded-lg px-4 py-3 focus:border-gold focus:ring-1 focus:ring-gold outline-none transition-colors",
                        placeholder: "email@example.com"
                    })]
                }), i.jsxs("div", {
                    children: [i.jsx("label", {
                        className: "block text-gray-400 mb-2 font-bold",
                        children: "الرسالة"
                    }), i.jsx("textarea", {
                        rows: 4,
                        className: "w-full bg-charcoal text-white border border-gray-700 rounded-lg px-4 py-3 focus:border-gold focus:ring-1 focus:ring-gold outline-none transition-colors",
                        placeholder: "كيف يمكننا مساعدتك؟"
                    })]
                }), i.jsx("button", {
                    className: "w-full bg-gold text-charcoal font-bold text-lg py-4 rounded-lg hover:bg-gold-light transition-colors shadow-lg",
                    children: "إرسال الرسالة"
                })]
            }), i.jsx("p", {
                className: "text-center text-gray-600 text-xs mt-6",
                children: "* سيتم استخدام هذه البيانات لأغراض العرض الأكاديمي فقط كجزء من مشروع التخرج."
            })]
        })
    })
})
  , bm = () => i.jsx("div", {
    className: "pt-24 pb-20 bg-charcoal min-h-screen flex items-center justify-center text-center",
    children: i.jsx("div", {
        className: "container mx-auto px-6",
        children: i.jsxs("div", {
            className: "max-w-xl mx-auto bg-white rounded-3xl p-10 shadow-2xl relative overflow-hidden",
            children: [i.jsx("div", {
                className: "absolute top-0 left-0 w-full h-2 bg-gradient-to-r from-gold to-riyadh-purple"
            }), i.jsx("div", {
                className: "mb-6 flex justify-center",
                children: i.jsx("div", {
                    className: "w-20 h-20 bg-green-100 rounded-full flex items-center justify-center",
                    children: i.jsx(La, {
                        className: "w-10 h-10 text-green-500"
                    })
                })
            }), i.jsx("h2", {
                className: "text-3xl font-bold font-heading text-charcoal mb-4",
                children: "تم تأكيد طلبك بنجاح!"
            }), i.jsx("p", {
                className: "text-gray-500 font-body mb-8 text-lg",
                children: "شكراً لحجزك في فعاليات الرياض. تم إرسال تفاصيل التذكرة إلى بريدك الإلكتروني."
            }), i.jsxs("div", {
                className: "bg-gray-50 p-6 rounded-2xl mb-8 border border-gray-100",
                children: [i.jsxs("div", {
                    className: "flex justify-between mb-2",
                    children: [i.jsx("span", {
                        className: "text-charcoal font-bold",
                        children: "رقم الطلب:"
                    }), i.jsx("span", {
                        className: "text-gray-500",
                        children: "#ORD-2025-8834"
                    })]
                }), i.jsxs("div", {
                    className: "flex justify-between",
                    children: [i.jsx("span", {
                        className: "text-charcoal font-bold",
                        children: "الحالة:"
                    }), i.jsx("span", {
                        className: "text-green-600 font-bold",
                        children: "مدفوع"
                    })]
                })]
            }), i.jsxs(Lt, {
                to: "/",
                className: "inline-flex items-center justify-center bg-charcoal text-white font-bold px-8 py-3 rounded-xl hover:bg-gold hover:text-charcoal transition-all",
                children: [i.jsx(dx, {
                    className: "w-5 h-5 ml-2"
                }), "العودة للرئيسية"]
            })]
        })
    })
})
  , Vx = () => {
    const {id: s} = t1()
      , d = Ks()
      , [o,f] = M.useState(null)
      , [m,g] = M.useState(!1);
    return M.useEffect( () => {
        const p = Ce.find(T => T.id === s);
        p ? f(p) : d("/events")
    }
    , [s, d]),
    o ? i.jsxs("div", {
        className: "bg-soft-gray min-h-screen animate-fade-in",
        children: [i.jsxs("div", {
            className: "relative h-[60vh] min-h-[400px]",
            children: [i.jsx("img", {
                src: o.image,
                alt: o.title,
                className: "w-full h-full object-cover"
            }), i.jsx("div", {
                className: "absolute inset-0 bg-gradient-to-t from-charcoal via-charcoal/50 to-transparent"
            }), i.jsx("div", {
                className: "absolute inset-0 bg-gradient-to-b from-black/60 via-transparent to-transparent h-32"
            }), i.jsxs("div", {
                className: "absolute bottom-0 left-0 right-0 p-6 md:p-12 container mx-auto",
                children: [i.jsxs(Lt, {
                    to: "/events",
                    className: "inline-flex items-center text-gray-300 hover:text-gold mb-6 transition-colors font-bold text-sm",
                    children: [i.jsx(ex, {
                        className: "w-4 h-4 ml-2"
                    }), "العودة للفعاليات"]
                }), i.jsxs("div", {
                    className: "flex flex-col md:flex-row md:items-end md:justify-between gap-6",
                    children: [i.jsxs("div", {
                        children: [i.jsx("span", {
                            className: "bg-gold text-charcoal font-bold px-4 py-1 rounded-full text-sm mb-4 inline-block",
                            children: o.type
                        }), i.jsx("h1", {
                            className: "text-4xl md:text-6xl font-heading font-bold text-white mb-2 leading-tight",
                            children: o.title
                        }), i.jsx("p", {
                            className: "text-gray-300 text-lg md:text-xl font-body max-w-2xl",
                            children: o.description
                        })]
                    }), i.jsx("div", {
                        className: "flex gap-4",
                        children: i.jsx("button", {
                            className: "bg-white/10 backdrop-blur-md text-white p-3 rounded-full hover:bg-white/20 transition-colors border border-white/20",
                            children: i.jsx(zx, {
                                className: "w-6 h-6"
                            })
                        })
                    })]
                })]
            })]
        }), i.jsx("div", {
            className: "container mx-auto px-6 -mt-10 relative z-10",
            children: i.jsxs("div", {
                className: "grid grid-cols-1 lg:grid-cols-3 gap-8",
                children: [i.jsxs("div", {
                    className: "lg:col-span-2 space-y-8",
                    children: [i.jsxs("div", {
                        className: "bg-white rounded-3xl p-8 shadow-xl",
                        children: [i.jsx("h2", {
                            className: "text-2xl font-heading font-bold text-charcoal mb-6 border-b border-gray-100 pb-4",
                            children: "تفاصيل الفعالية"
                        }), i.jsxs("p", {
                            className: "text-gray-600 leading-relaxed text-lg mb-6",
                            children: ["استعد لتجربة استثنائية في ", o.title, ". انضم إلينا في ", o.location, " لقضاء وقت لا ينسى. هذه الفعالية تعتبر واحدة من أبرز محطات موسم الرياض لهذا العام، حيث تجمع بين الترفيه والإبداع في مكان واحد."]
                        }), i.jsx("p", {
                            className: "text-gray-600 leading-relaxed text-lg",
                            children: "تتميز الفعالية بتنظيم عالمي المستوى، وتوفر مرافق متكاملة لخدمة الزوار، بما في ذلك مناطق للمطاعم والمقاهي، ومواقف سيارات واسعة، وخدمات ذوي الاحتياجات الخاصة. لا تفوت الفرصة لتكون جزءاً من هذا الحدث الضخم."
                        }), i.jsxs("div", {
                            className: "mt-8 grid grid-cols-1 md:grid-cols-2 gap-6",
                            children: [i.jsx("img", {
                                src: `https://picsum.photos/seed/${o.id}1/800/400`,
                                alt: "Gallery 1",
                                className: "rounded-xl object-cover h-48 w-full hover:scale-105 transition-transform duration-500 cursor-pointer"
                            }), i.jsx("img", {
                                src: `https://picsum.photos/seed/${o.id}2/800/400`,
                                alt: "Gallery 2",
                                className: "rounded-xl object-cover h-48 w-full hover:scale-105 transition-transform duration-500 cursor-pointer"
                            })]
                        })]
                    }), i.jsxs("div", {
                        className: "bg-white rounded-3xl p-8 shadow-xl",
                        children: [i.jsx("h2", {
                            className: "text-2xl font-heading font-bold text-charcoal mb-6 border-b border-gray-100 pb-4",
                            children: "الموقع على الخريطة"
                        }), i.jsx("div", {
                            className: "rounded-xl h-80 overflow-hidden shadow-md border border-gray-200 relative",
                            children: o.mapUrl ? i.jsx("iframe", {
                                src: o.mapUrl,
                                className: "w-full h-full",
                                style: {
                                    border: 0
                                },
                                allowFullScreen: !0,
                                loading: "lazy",
                                referrerPolicy: "no-referrer-when-downgrade",
                                title: `Map location for ${o.title}`
                            }) : i.jsx("div", {
                                className: "w-full h-full flex items-center justify-center bg-gray-100",
                                children: i.jsxs("div", {
                                    className: "text-center",
                                    children: [i.jsx(ta, {
                                        className: "w-12 h-12 text-gray-400 mx-auto mb-2"
                                    }), i.jsx("span", {
                                        className: "text-gray-500 font-bold",
                                        children: o.location
                                    }), i.jsx("p", {
                                        className: "text-xs text-gray-400 mt-2",
                                        children: "الخريطة غير متوفرة حالياً"
                                    })]
                                })
                            })
                        })]
                    })]
                }), i.jsx("div", {
                    className: "lg:col-span-1",
                    children: i.jsxs("div", {
                        className: "bg-white rounded-3xl p-8 shadow-xl sticky top-24 border-t-4 border-gold",
                        children: [i.jsx("h3", {
                            className: "text-xl font-heading font-bold text-charcoal mb-6",
                            children: "معلومات التذاكر"
                        }), i.jsxs("div", {
                            className: "space-y-6 mb-8",
                            children: [i.jsxs("div", {
                                className: "flex items-center text-right",
                                children: [i.jsx("div", {
                                    className: "bg-soft-gray p-3 rounded-full ml-4",
                                    children: i.jsx(gi, {
                                        className: "w-6 h-6 text-gold"
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("span", {
                                        className: "block text-xs text-gray-500 font-bold mb-1",
                                        children: "التاريخ"
                                    }), i.jsx("span", {
                                        className: "font-bold text-charcoal text-lg",
                                        children: o.date
                                    })]
                                })]
                            }), i.jsxs("div", {
                                className: "flex items-center text-right",
                                children: [i.jsx("div", {
                                    className: "bg-soft-gray p-3 rounded-full ml-4",
                                    children: i.jsx(Fs, {
                                        className: "w-6 h-6 text-gold"
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("span", {
                                        className: "block text-xs text-gray-500 font-bold mb-1",
                                        children: "الوقت"
                                    }), i.jsx("span", {
                                        className: "font-bold text-charcoal text-lg",
                                        children: o.time
                                    })]
                                })]
                            }), i.jsxs("div", {
                                className: "flex items-center text-right",
                                children: [i.jsx("div", {
                                    className: "bg-soft-gray p-3 rounded-full ml-4",
                                    children: i.jsx(ta, {
                                        className: "w-6 h-6 text-gold"
                                    })
                                }), i.jsxs("div", {
                                    children: [i.jsx("span", {
                                        className: "block text-xs text-gray-500 font-bold mb-1",
                                        children: "الموقع"
                                    }), i.jsx("span", {
                                        className: "font-bold text-charcoal text-lg",
                                        children: o.location
                                    })]
                                })]
                            })]
                        }), i.jsxs("div", {
                            className: "bg-gray-50 p-4 rounded-xl border border-gray-200 text-center mb-6",
                            children: [i.jsx("span", {
                                className: "block text-gray-500 text-sm mb-1",
                                children: "يبدأ سعر التذكرة من"
                            }), i.jsx("span", {
                                className: "block text-2xl font-bold text-gold",
                                children: o.price
                            })]
                        }), i.jsxs("button", {
                            onClick: () => g(!0),
                            className: "w-full bg-charcoal text-white font-bold py-4 rounded-xl hover:bg-gold hover:text-charcoal transition-all shadow-lg flex items-center justify-center gap-2",
                            children: [i.jsx(Ox, {
                                className: "w-5 h-5"
                            }), "احجز تذكرتك الآن"]
                        }), i.jsx("p", {
                            className: "text-center text-xs text-gray-400 mt-4",
                            children: "* تطبق الشروط والأحكام"
                        })]
                    })
                })]
            })
        }), i.jsx(Is, {
            event: o,
            isOpen: m,
            onClose: () => g(!1)
        })]
    }) : null
}
  , Kx = () => {
    const {pathname: s} = sl();
    return M.useEffect( () => {
        window.scrollTo(0, 0)
    }
    , [s]),
    null
}
  , Jx = () => i.jsx(B1, {
    children: i.jsxs("div", {
        className: "font-body text-right min-h-screen flex flex-col",
        children: [i.jsx(Kx, {}), i.jsx(Ux, {}), i.jsx("main", {
            className: "flex-grow",
            children: i.jsxs(g1, {
                children: [i.jsx(Be, {
                    path: "/",
                    element: i.jsx(Yx, {})
                }), i.jsx(Be, {
                    path: "/events",
                    element: i.jsx(Lx, {})
                }), i.jsx(Be, {
                    path: "/events/:id",
                    element: i.jsx(Vx, {})
                }), i.jsx(Be, {
                    path: "/events/:id/order",
                    element: i.jsx(bm, {})
                }), i.jsx(Be, {
                    path: "/calendar",
                    element: i.jsx(Gx, {})
                }), i.jsx(Be, {
                    path: "/qiddiya",
                    element: i.jsx(Xx, {})
                }), i.jsx(Be, {
                    path: "/about",
                    element: i.jsx(Qx, {})
                }), i.jsx(Be, {
                    path: "/contact",
                    element: i.jsx(Zx, {})
                }), i.jsx(Be, {
                    path: "/order",
                    element: i.jsx(bm, {})
                })]
            })
        }), i.jsx(Hx, {})]
    })
})
  , Xm = document.getElementById("root");
if (!Xm)
    throw new Error("Could not find root element to mount to");
const kx = jg.createRoot(Xm);
kx.render(i.jsx(gg.StrictMode, {
    children: i.jsx(Jx, {})
}));
